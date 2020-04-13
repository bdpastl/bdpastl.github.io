# Tic Tac Toe: 

### Creating the project: 

Click into the File >> New Project: 

![newProject](/Users/mjlane/Desktop/newProject.png)



In the helper, navigate to the new JavaFX Project: ![newJavaFXProject](/Users/mjlane/Desktop/newJavaFXProject.png)



Select a name for your java project. Make sure you're using the right JRE (how to do this is noted in the installation guide): 

![createNewFXProject](/Users/mjlane/Desktop/createNewFXProject.png)

You'll notice that there are a ton of errors:

![buildErrorsFX](/Users/mjlane/Desktop/buildErrorsFX.png)





 To fix this, right click your project and navigate to build path, and click `Add Libraries`: 

![buildPath](/Users/mjlane/Desktop/buildPath.png)

After clicking into add libraries, click user library: ![userLibrary](/Users/mjlane/Desktop/userLibrary.png)

Now select the desired JavaFX library: 

![selectJavaFX](/Users/mjlane/Desktop/selectJavaFX.png)



Now your app ought to be able to run! Make sure that your code looks like the below code with no errors: 

```java
package application;
	
import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.BorderPane;


public class Main extends Application {
	@Override
	public void start(Stage primaryStage) {
		try {
			BorderPane root = new BorderPane();
			Scene scene = new Scene(root,1000,1000);
			scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
			primaryStage.setScene(scene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}

```



Now click the run button and you should see a blank pane (very exciting): 

![blankPane](/Users/mjlane/Desktop/blankPane.png)

### Writing the code! 

Let's first start out by cleaning up our `start` method and  making our pane a bit smaller by changing the size of our window to 500 by 500: 

```java
package application;
	
import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.Pane;


public class Main extends Application {
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,500,500);
	scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		return scene; 
	}
	
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}

```



Tic Tac Toe has a three by three grid of `X`s and `O`s, so let's create each individual grid by creating a private class called Tile: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;


public class Main extends Application {
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		return scene; 
	}
	
	
	private class Tile extends StackPane {
		public Tile() {
			Rectangle border = new Rectangle(200,200);
			border.setFill(null); 
			border.setStroke(Color.BLACK);
			
			setAlignment(Pos.CENTER); 
			getChildren().addAll(border); 
		}
		
	}
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}

```





Now let's add our tiles to our border! 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;


public class Main extends Application {
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
						
				root.getChildren().add(tile); 
			}
		}

		return scene; 
	}
	
	
	private class Tile extends StackPane {
		public Tile() {
			Rectangle border = new Rectangle(200,200);
			border.setFill(null); 
			border.setStroke(Color.BLACK);
			
			setAlignment(Pos.CENTER); 
			getChildren().addAll(border); 
		}
	}
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
      
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```



Now, when a user clicks a specific tile, that tile ought to show either `X` or `O`. To do that, we'll need to add text to our tiles: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Text;


public class Main extends Application {
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
				
				root.getChildren().add(tile); 
			}
		}
		
		return scene; 
	}
	
	
	class Tile extends StackPane {
		Text text = new Text(); 
		
		public Tile() {
			Rectangle border = new Rectangle(200,200);
			border.setFill(null); 
			border.setStroke(Color.BLACK);
			
			setAlignment(Pos.CENTER); 
			getChildren().addAll(border); 
	
		}
		
		private void drawX() {
			text.setText("X");
		}
		
		private void drawO() {
			text.setText("O");
		}
	}
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```



We've added text to our tile, but there's nothing calling setText for `X` or `O`. In order to do that, we'll need to add in some event driven programming. To do that, we'll need to add a function to our tile constructor called `setOnMouseClicked` that takes in a function. In this function, we'll use a lambda to actually set our text by calling those methods: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Text;


public class Main extends Application {
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
				
				root.getChildren().add(tile); 
			}
		}
		
		return scene; 
	}
	
	
	class Tile extends StackPane {
		Text text = new Text(); 
		
		public Tile() {
			Rectangle border = new Rectangle(200,200);
			border.setFill(null); 
			border.setStroke(Color.BLACK);
			
			setAlignment(Pos.CENTER); 
			getChildren().addAll(border, text); 
			
			setOnMouseClicked(eventClick -> {
				System.out.println("What is the event?" + eventClick);
				if (eventClick.getButton() == MouseButton.PRIMARY) {
					drawX(); 
				} else {
					drawO(); 
				}
			});	
		}
		
		private void drawX() {
			text.setText("X");
		}
		
		private void drawO() {
			text.setText("O");
		}
	}
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```



Clearly we need to increase the size of our `X`s and `O`s. Let's do that by using the `text.setFont`method inside of our tile constructor: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;


public class Main extends Application {
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
				
				root.getChildren().add(tile); 
			}
		}
		
		return scene; 
	}

	
	class Tile extends StackPane {
		Text text = new Text(); 
		
		public Tile() {
			Rectangle border = new Rectangle(200,200);
			border.setFill(null); 
			border.setStroke(Color.BLACK);
			
			text.setFont(Font.font(72));
			
			setAlignment(Pos.CENTER); 
			getChildren().addAll(border, text); 
			
			setOnMouseClicked(eventClick -> {
				System.out.println("What is the event?" + eventClick);
				if (eventClick.getButton() == MouseButton.PRIMARY) {
					drawX(); 
				} else {
					drawO(); 
				}
			});	
		}
		
		private void drawX() {
			text.setText("X");
		}
		
		private void drawO() {
			text.setText("O");
		}
	}
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```

You may have noticed, though, that you can literally click any single spot on the game board and change it to either `X` or `O`. So let's create a method that makes it so that you absolutely must change the turn of who's playing: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;


public class Main extends Application {
	
	private boolean turnX = true; 
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
				
				root.getChildren().add(tile); 
			}
		}
		
		return scene; 
	}

	
	class Tile extends StackPane {
		Text text = new Text(); 
		
		public Tile() {
			Rectangle border = new Rectangle(200,200);
			border.setFill(null); 
			border.setStroke(Color.BLACK);
			
			text.setFont(Font.font(72));
			
			setAlignment(Pos.CENTER); 
			getChildren().addAll(border, text); 
			
			setOnMouseClicked(eventClick -> {
				System.out.println("What is the event?" + eventClick);
				if (eventClick.getButton() == MouseButton.PRIMARY) {
					if(!turnX) {
						return; 
					}
					
					drawX(); 
					turnX = false; 
				} else {
					if(turnX) {
						return;
					}
					drawO(); 
					turnX = true; 
				}
			});	
		}
		
		private void drawX() {
			text.setText("X");
		}
		
		private void drawO() {
			text.setText("O");
		}
	}
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```

 

When we run the program, now we can't play multiple runs of `X` or `O`! We're not out of the woods yet, you can still overwrite spaces! So let's make sure that our spaces are playable before we set the text! 

It seems though, now, that we need a way to determine whether the space is playable or not. A good way to see if a space is playable is to determine whether or not there's any text in the space itself, so let's write a getter function for the tile's text, and a function that returns a boolean if the tile already has text in it: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;


public class Main extends Application {
	private boolean turnX = true; 
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
				
				root.getChildren().add(tile); 
			}
		}
		
		return scene; 
	}


	class Tile extends StackPane {
		Text text = new Text(); 
		
		public Tile() {
			Rectangle border = new Rectangle(200,200);
			border.setFill(null); 
			border.setStroke(Color.BLACK);
			
			text.setFont(Font.font(72));
			
			setAlignment(Pos.CENTER); 
			getChildren().addAll(border, text); 
			
			setOnMouseClicked(eventClick -> {
				if(!isPlayableSpace()) return; 
				
				System.out.println("What is the event?" + eventClick);
				if (eventClick.getButton() == MouseButton.PRIMARY) {
					if(!turnX) {
						return; 
					}		
					drawX(); 
					turnX = false; 
				} else {
					if(turnX) {
						return;
					}
					drawO(); 
					turnX = true; 
				}
			});	
		}
		
		private void drawX() {
			text.setText("X");
		}
		
		private void drawO() {
			text.setText("O");
		}
		
		public String getTextValue() {
			return text.getText(); 
		}
		
		public boolean isPlayableSpace() {
			if( getTextValue().isEmpty() ) {
				return true; 
			}
			return false; 
		}
	}
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```



So now that we've build the basic game board, we need to find a way to determine who the winner is! However, before we do that, let's try refactoring our code first. Refactoring doesn't just include renaming things, it also includes moving bits of code around, rewriting functions to be more abstract, etc. So, let's start by moving our Tile class into it's own class outside of our main application file. 

`Tile.java`

```java
package application;

import javafx.geometry.Pos;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;


public class Tile extends StackPane {	
	public Tile() {
		Rectangle border = new Rectangle(200,200);
		border.setFill(null); 
		border.setStroke(Color.BLACK);
		
		text.setFont(Font.font(72));
		
		setAlignment(Pos.CENTER); 
		getChildren().addAll(border, text); 
		
		setOnMouseClicked(eventClick -> {
			if(!isPlayableSpace()) return; 
			
			System.out.println("What is the event?" + eventClick);
			if (eventClick.getButton() == MouseButton.PRIMARY) {
				if(!Turn.turnX) {
					return; 
				}
				
				drawX(); 
				turnX = false; 
			} else {
				if(turnX) {
					return;
				}
				drawO(); 
				turnX = true; 
			}
		});	
	}
	
	private void drawX() {
		text.setText("X");
	}
	
	private void drawO() {
		text.setText("O");
	}
	
	public String getTextValue() {
		return text.getText(); 
	}
	
	public boolean isPlayableSpace() {
		if( getTextValue().isEmpty() ) {
			return true; 
		}
		return false; 
	}
}
```



The above is great! Though we do seem to have run into a snag, since our turnX was an application level boolean value. How do we share something between a whole number of references? If we tried to place turnX within our Tile class we would be creating a new `turnX` boolean every single time a new class was instantiated. UNLESS we make it static! So let's do that: 

`Tile.java`: 

```java
package application;

import javafx.geometry.Pos;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;

public class Tile extends StackPane {
	static boolean turnX = true; 
	
	Text text = new Text(); 
	
	public Tile() {
		Rectangle border = new Rectangle(200,200);
		border.setFill(null); 
		border.setStroke(Color.BLACK);
		
		text.setFont(Font.font(72));
		
		setAlignment(Pos.CENTER); 
		getChildren().addAll(border, text); 
		
		setOnMouseClicked(eventClick -> {
			if(!isPlayableSpace()) return; 
			
			System.out.println("What is the event?" + eventClick);
			if (eventClick.getButton() == MouseButton.PRIMARY) {
				if(!turnX) {
					return; 
				}
				
				drawX(); 
				turnX = false; 
			} else {
				if(turnX) {
					return;
				}
				drawO(); 
				turnX = true; 
			}
		});	
	}
	
	private void drawX() {
		text.setText("X");
	}
	
	private void drawO() {
		text.setText("O");
	}
	
	public String getTextValue() {
		return text.getText(); 
	}
	
	public boolean isPlayableSpace() {
		if( getTextValue().isEmpty() ) {
			return true; 
		}
		return false; 
	}
}

```

Deleting the tile code out of our main function, it looks a lot cleaner: 

`Main.java`: 

```java
package application;
	
import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.Pane;


public class Main extends Application {
	
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
				
				root.getChildren().add(tile); 
			}
		}
		
		return scene; 
	}

	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```



Now that our code's a bit cleaner, let's write some code to determine if there are three spaces in a row that all have the same exact text! We could write a method to do this, but let's instead create a class to take in 3 cards as a parameter for its constructor, and then determine whether those three cards are all the same type! 

`ThreeInARow.java`

```java
package application;


class ThreeInARow {
	private Tile[] tiles; 
	
	public ThreeInARow(Tile... tiles) {  // varargs - VARANEAT
		this.tiles = tiles; 
	}
	
	public boolean hasWinningCondition() {
		if (tiles[0].getTextValue().isEmpty()) return false; 
System.out.println(tiles[0].getTextValue() + " " + tiles[1].getTextValue() + " " + tiles[2].getTextValue());
		boolean isWinner = tiles[0].getTextValue().equals(tiles[1].getTextValue()) && 
				tiles[0].getTextValue().equals(tiles[2].getTextValue());

		return isWinner; 
	}
}

```

In the above code, you'll notice a brand new construction that we haven't talked about before. That's the varargs operator. That operator essentially says that there will be some kind of list of objects coming in of some type (in this case, tile). 



Now let's some code to determine a winner! There are multiple possible winning conditions. Let's write a class that has a list of all possible winning conditions AND a way to check for a winner! We'll do so by having an arrayList of `ThreeInARow` objects and have a method that checks if any of those `ThreeInARow` objects return true on `hasWinningCondition`. 

`CheckWinningCondition.java`

```java
package application;

import java.util.ArrayList;
import java.util.List;

public class CheckWinningCondition {
	public static List<ThreeInARow> threeInARowList = new ArrayList<ThreeInARow>(); 
	
	public static void checkWinner() {
		// Go through all possible combinations! 
		for(ThreeInARow combination : threeInARowList ) {
			if(combination.hasWinningCondition()) {
				System.out.println("OH GOODNESS THERE'S A WINNER!"); 

				break;
			} 
		}
	}	
}
```



Now that we have a way to create these possible winning conditions, let's add all the possible winning conditions to our list in main! The first being all three possible rows, all three possible columns, and the two diagonals!

`Main.java`

```java
package application;
	
import java.util.ArrayList;
import java.util.List;

import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.Pane;


public class Main extends Application {
	private Tile[][] board = new Tile[3][3]; 
	
	private boolean gameWinner = false; /// ???????
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane();
		Scene scene = new Scene(root,600,600);
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
		
		// Create new tiles within the scene! 
		for (int i = 0 ; i < 3; i++) {
			for (int j = 0 ; j < 3; j++ ) {
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
				
				root.getChildren().add(tile);
				
				board[j][i] = tile;  // this way we assign an element to the array's value. 
			}
		}
		
		
		// for all horizontal rows: 
		for (int y = 0 ; y < 3; y++) {
			ThreeInARow threeInARowObject = new ThreeInARow( board[0][y], board[1][y], board[2][y]);
			CheckWinningCondition.threeInARowList.add(threeInARowObject); 
		}
		
		// for all vertical columns: 
		for (int x = 0 ; x < 3; x++) {
			ThreeInARow threeInARowObject = new ThreeInARow( board[x][0], board[x][1], board[x][2]);
			CheckWinningCondition.threeInARowList.add(threeInARowObject); 
		}

		// for the diagonals: 
		ThreeInARow diagonalThreeInARow = new ThreeInARow( board[0][0], board[1][1], board[2][2]);
		CheckWinningCondition.threeInARowList.add(diagonalThreeInARow); 
		
		
		ThreeInARow diagonalThreeInARowOpposite = new ThreeInARow( board[2][0], board[1][1], board[0][2]);
		CheckWinningCondition.threeInARowList.add(diagonalThreeInARow); 
		return scene; 
	}


	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene myScene = buildPrimaryStageScene(); 
			
			primaryStage.setScene(myScene);
			primaryStage.show();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```



If we were tor run the program now, we'd wind up having some difficulty, finding out who our winner is because we need to do one more step... and that's calling the `checkWinner` method! You may have wondered why we made the check winning condition and the list static, and that's because we want only a single instance of it so that we can access it easily across all classes! 

`Tile.java`

```java
package application;

import javafx.geometry.Pos;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;

public class Tile extends StackPane {
	static boolean turnX = true; 
	
	Text text = new Text(); 
	
	public Tile() {
		Rectangle border = new Rectangle(200,200);
		border.setFill(null); 
		border.setStroke(Color.BLACK);
		
		text.setFont(Font.font(72));
		
		setAlignment(Pos.CENTER); 
		getChildren().addAll(border, text); 
		
		setOnMouseClicked(eventClick -> {
			if(!isPlayableSpace()) return; 
			
			System.out.println("What is the event?" + eventClick);
			if (eventClick.getButton() == MouseButton.PRIMARY) {
				if(!turnX) {
					return; 
				}
				
				drawX(); 
				turnX = false; 
				CheckWinningCondition.checkWinner();

			} else {
				if(turnX) {
					return;
				}
				drawO(); 
				turnX = true;
				CheckWinningCondition.checkWinner();
			}
		});	
	}
	
	private void drawX() {
		text.setText("X");
	}
	
	private void drawO() {
		text.setText("O");
	}
	
	public String getTextValue() {
		return text.getText(); 
	}
	
	public boolean isPlayableSpace() {
		if( getTextValue().isEmpty() ) {
			return true; 
		}
		return false; 
	}
}
```



So now when we run the program, you should try to get a winning condition! If the game has one (that is, if you get three in a row), "OH GOODNESS THERE'S A WINNER" will be printed to our console! However, the game doesn't seem to stop at all, so let's add one more static boolean so that we can see if the game's won across all of our classes and set it to true when we reach our winning condition. 

`CheckWinningCondition.java`

```java
package application;

import java.util.ArrayList;
import java.util.List;

public class CheckWinningCondition {
	public static List<ThreeInARow> threeInARowList = new ArrayList<ThreeInARow>(); 
	public static boolean gameIsWon = false; 
	
	public static void checkWinner() {
		// Go through all possible combinations! 
		for(ThreeInARow combination : threeInARowList ) {
			if(combination.hasWinningCondition()) {
				System.out.println("OH GOODNESS THERE'S A WINNER!"); 
				gameIsWon = true; 
				break;
			} 
		}
	}	
}
```

To make sure we stop the game, we'll need to access this boolean in our Tile class and make sure we don't allow for `setOnMouseClicked` to run if there has been a winner. We've already done so for `isPlayableSpace`, so let's just add our boolean check into that: 

`Tile.java`

```java
package application;

import javafx.geometry.Pos;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;

public class Tile extends StackPane {
	static boolean turnX = true; 
	
	Text text = new Text(); 
	
	public Tile() {
		Rectangle border = new Rectangle(200,200);
		border.setFill(null); 
		border.setStroke(Color.BLACK);
		
		text.setFont(Font.font(72));
		
		setAlignment(Pos.CENTER); 
		getChildren().addAll(border, text); 
		
		setOnMouseClicked(eventClick -> {
			if(!isPlayableSpace() || CheckWinningCondition.gameIsWon) return; 
			
			System.out.println("What is the event?" + eventClick);
			if (eventClick.getButton() == MouseButton.PRIMARY) {
				if(!turnX) {
					return; 
				}
				
				drawX(); 
				turnX = false; 
				CheckWinningCondition.checkWinner();

			} else {
				if(turnX) {
					return;
				}
				drawO(); 
				turnX = true;
				CheckWinningCondition.checkWinner();
			}
		});	
	}
	
	private void drawX() {
		text.setText("X");
	}
	
	private void drawO() {
		text.setText("O");
	}
	
	public String getTextValue() {
		return text.getText(); 
	}
	
	public boolean isPlayableSpace() {
		if( getTextValue().isEmpty() ) {
			return true; 
		}
		return false; 
	}
}
```



Before we move to our animation, let's refactor our main class a little bit just to make it a bit more clean: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.BorderPane;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;


public class Main extends Application {
	private Tile[][] board = new Tile[3][3]; 
	
	
	
	public void addTilesToTIARList() {

		for (int i = 0 ; i < 3; i++ ) {
			ThreeInARow threeInARowObject = new ThreeInARow(	
				board[0][i],
				board[1][i],
				board[2][i]
			);	

			ThreeInARow threeInARowObjectColumn = new ThreeInARow(	
				board[i][0],
				board[i][1],
				board[i][2]
			);
			
			CheckWinningCondition.threeInARowList.add(threeInARowObjectColumn);
			CheckWinningCondition.threeInARowList.add(threeInARowObject);
		}
	
		ThreeInARow diagonalThreeInARow = new ThreeInARow(
				board[0][0],
				board[1][1],
				board[2][2]
		);
			
		ThreeInARow reverseDiagonalThreeIAR = new ThreeInARow(
				board[0][2],
				board[1][1],
				board[2][0]
		);
		
		CheckWinningCondition.threeInARowList.add(diagonalThreeInARow);
		CheckWinningCondition.threeInARowList.add(reverseDiagonalThreeIAR);
	}
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane(); 
		Scene scene = new Scene(root, 600, 600); 
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
	
		for(int i = 0 ; i < 3; i++) {
			for(int j = 0 ; j < 3; j++){
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
			
				root.getChildren().add(tile);
				
				board[j][i] = tile; 
			}	
		}

		addTilesToTIARList();
		return scene; 
	}
	
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene scene = buildPrimaryStageScene(); 

			primaryStage.setScene(scene);
			primaryStage.show();
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}

```



### Adding Animations: 

Fun story, nobody will be looking at the console to see if there's a winner, and if the game just stops, they might not know there's a winner, so we'll need to add one more step. When someone wins the game, we'll need to add an animation to show that we have a winning condition! For the sake of easiness, let's just make it a big line through the winning tiles! 

To do this, we'll need to create an animation that goes through all three points in our tiles. First, though, we'll need to get the center of each of our tiles so that we'll have a starting and ending point for our lines: 

`Tile.java`: 

```java
package application;

import javafx.geometry.Pos;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;


class Tile extends StackPane {
	static boolean turnX = true; 
	Text text = new Text(); 
	
	public Tile() {
		Rectangle border = new Rectangle(200,200); 
		border.setFill(null);
		border.setStroke(Color.BLACK);
		text.setFont(Font.font(120));
		
		
		setAlignment(Pos.CENTER); 
		getChildren().addAll(border, text);
		
		setOnMouseClicked(eventClick -> {
			if( !isPlayableSpace() || CheckWinningCondition.gameIsWon ) return; 
				
			System.out.println("eventClick?" + eventClick);
			if(eventClick.getButton() == MouseButton.PRIMARY) {
				if (! turnX ) return; 
				
				drawX(); 
				CheckWinningCondition.checkWinner();
				turnX = false; 
			} else {
				if ( turnX ) return; 
				
				drawO();
				CheckWinningCondition.checkWinner();
				turnX = true; 
			}
			
		});
	}
	
	
	private void drawX() {
		text.setText("X");
	}
	
	private void drawO() {
		text.setText("O");
	}
	
	public String getTextValue() {
		return text.getText();
	}
	
	public boolean isPlayableSpace() {
		if( getTextValue().isEmpty() ) {
			return true; 
		}
		
		return false; 
	}
	
	public double getCenterX() {
		return getTranslateX() + (200 / 2); 
	}
	
	public double getCenterY() {
		return getTranslateY() + (200 / 2); 
	}	
}
```



Now that we have our center values, we can use those to create our line! Though because we're doing an animation, we'll want to have both the start and the end of our line be on the very first tile's center values. Then, after establishing that our line exists, we'll create a couple of Key values with our end X and end Y coordinates from our tile. We then want to put those key values into a key frame with a duration of how long we want the animation to last.  Finally, we'll add that key frame to our timeline, and then play the animation! 

Before that will actually work though, we'll need to add our line to the child nodes of our root pane! So, we'll create a function to do that as well! 

`CheckWinningCondtition.java`

```java
package application;

import java.util.ArrayList;
import java.util.List;

import javafx.animation.Interpolator;
import javafx.animation.KeyFrame;
import javafx.animation.KeyValue;
import javafx.animation.Timeline;
import javafx.scene.layout.Pane;
import javafx.scene.shape.Line;
import javafx.util.Duration;

public class CheckWinningCondition {
	public static List<ThreeInARow> threeInARowList = new ArrayList<ThreeInARow>();
	public static boolean gameIsWon = false; 
	public static Line winningLine = new Line(); 
	
	
	public static void checkWinner() {
		for (ThreeInARow combination : threeInARowList) {
			
			if(combination.hasWinningCondition()){
				System.out.println("OH GOODNESS! THERE'S A WINNER!");
				
				gameIsWon = true; 
				playWinningAnimation(combination);
				break;
			}
		}
	}
	
	private static void playWinningAnimation(ThreeInARow threeInARow) {
		for (Tile tile : threeInARow.tiles) {
			double xCoords = tile.getCenterX(); 
			double yCoords = tile.getCenterY(); 
			System.out.println( " X : " + xCoords + " Y: " + yCoords); 
		}

		winningLine.setStartX(threeInARow.tiles[0].getCenterX());
		winningLine.setStartY(threeInARow.tiles[0].getCenterY());
		winningLine.setEndX(threeInARow.tiles[0].getCenterX());
		winningLine.setEndY(threeInARow.tiles[0].getCenterY());
		winningLine.setStrokeWidth(15);
		
		
		KeyValue endX = new KeyValue(winningLine.endXProperty(), threeInARow.tiles[2].getCenterX());
        KeyValue endY = new KeyValue(winningLine.endYProperty(), threeInARow.tiles[2].getCenterY());
        
        KeyFrame timeLineKeyFrameAnimation = new KeyFrame(Duration.seconds(3), endX, endY);
        
        Timeline timeline =  new Timeline( timeLineKeyFrameAnimation);
        timeline.play();
	}
	

	public static void addLinesToRoot(Pane rootPane) {
		rootPane.getChildren().add(winningLine); 
	}
}

```



And then finally, we'll want to add it to our (very finely refactored) Main class: 

`Main.java`: 

```java
package application;
	
import javafx.application.Application;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.input.MouseButton;
import javafx.scene.layout.BorderPane;
import javafx.scene.layout.Pane;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;


public class Main extends Application {
	private Tile[][] board = new Tile[3][3]; 
	
	
	
	public void addTilesToTIARList() {

		for (int i = 0 ; i < 3; i++ ) {
			ThreeInARow threeInARowObject = new ThreeInARow(	
				board[0][i],
				board[1][i],
				board[2][i]
			);	

			ThreeInARow threeInARowObjectColumn = new ThreeInARow(	
				board[i][0],
				board[i][1],
				board[i][2]
			);
			
			CheckWinningCondition.threeInARowList.add(threeInARowObjectColumn);
			CheckWinningCondition.threeInARowList.add(threeInARowObject);
		}
	
		ThreeInARow diagonalThreeInARow = new ThreeInARow(
				board[0][0],
				board[1][1],
				board[2][2]
		);
			
		ThreeInARow reverseDiagonalThreeIAR = new ThreeInARow(
				board[0][2],
				board[1][1],
				board[2][0]
		);
		
		CheckWinningCondition.threeInARowList.add(diagonalThreeInARow);
		CheckWinningCondition.threeInARowList.add(reverseDiagonalThreeIAR);
	}
	
	
	
	
	public Scene buildPrimaryStageScene() {
		Pane root = new Pane(); 
		Scene scene = new Scene(root, 600, 600); 
		scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());

		
		
		for(int i = 0 ; i < 3; i++) {
			for(int j = 0 ; j < 3; j++){
				Tile tile = new Tile(); 
				tile.setTranslateX(j*200);
				tile.setTranslateY(i*200);
			
				root.getChildren().add(tile);
				
				board[j][i] = tile; 
			}	
		}

		addTilesToTIARList();
		CheckWinningCondition.addLinesToRoot(root);
		return scene; 
	}
	
	
	@Override
	public void start(Stage primaryStage) {
		try {
			Scene scene = buildPrimaryStageScene(); 

			primaryStage.setScene(scene);
			primaryStage.show();
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	
	public static void main(String[] args) {
		launch(args);
	}
}
```

