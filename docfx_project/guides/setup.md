## Azurite Project Setup Guide
This is just filler for now. 
### Code Samples
#### BoilerPlate Code:
```java
public class Main extends Scene {
	public static void main(String[] args) {
		Engine.init(1920, 1080, "Azurite Engine Demo In Comment", 1.0f);
		Engine.scenes().switchScene(new Main(), true);
		Engine.showWindow();
	}

	public void awake() {
		camera = new Camera();
		...
	}

	public void update() {
		...
	}
}
```

#### Simple example with sprites:
```java
public class Main extends Scene {
	GameObject player;
	Sprite s;

	public static void main(String[] args) {
		Engine.init(1920, 1080, "Azurite Engine Demo In Comment", 1.0f);
		Engine.scenes().switchScene(new Main(), true);
		Engine.showWindow();
	}

	public void awake() {
		camera = new Camera();

		player = new GameObject();
		s = new Sprite
		player.addComponent(new SpriteRenderer(s, new Vector2f(100)));
	}

	public void update() {
		if (Keyboard.getKeyDown(GLFW.GLFW_KEY_SPACE))
			player.transform.add(new Vector2f(1, 0));
	}
}