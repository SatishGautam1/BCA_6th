### Introducing Swing
- Java Swing is a part of Java Foundation Classes (JFC) that is used to create window-based applications. It is built on the top of AWT (Abstract Windowing Toolkit) API and entirely written in java.
- Unlike AWT, Java Swing provides platform-independent and lightweight components.
- The javax.swing package provides classes for java swing API such as JButton, JTextField, JTextArea, JRadioButton, JCheckBox, JMenu, JColorChooser etc.

#### Differences between AWT and Swing

| S.N.: | Java Awt                                                                                                                                                              | Java Swing                                                                                               |
| ----- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| 1     | AWT components are platform-dependent.                                                                                                                                | Java swing components are platform-independent.                                                          |
| 2     | AWT components are heavyweight.                                                                                                                                       | Swing components are lightweight.                                                                        |
| 3     | AWT doesn't support pluggable look and feel.                                                                                                                          | Swing supports pluggable look and feel.                                                                  |
| 4     | AWT providees less components than Swing.                                                                                                                             | Swing provides more powerful components such as tables, lists, scrollpanes, colorchooser, tabbepane etc. |
| 5     | AWT doesn't follows MVC (Model View Controller) where model represents data, view represents presentation and controller acts as an interface between model and view. | Swing follows MVC.                                                                                       |
#### JFC(Java Foundation Class)
The Java Foundation Classes (JFC) are a set of GUI components which simplify the development of desktop applications.

#### Hierarchy of Java Swing classes
![[Pasted image 20240625211143.png]]

#### Commonly used Methods of Component class

| Method                                     | Description                                                   |
| ------------------------------------------ | ------------------------------------------------------------- |
| public void add(Component c)               | add a component on another component                          |
| public void setSize(int width, int height) | sets size of the component                                    |
| public void setLayout(LayoutManager m)     | sets the layout manager for the component                     |
| public void setVisible(boolean b)          | sets the visibility of the component. It is by default false. |
### Creating a Frame
There are two ways to create a frame:
1. By creating the object of Frame class (association)
2. By extending Frame class (inheritance)
We can write the code of swing inside the main(), constructor or any other method.

Simple swing example: creating one button and adding it on the JFrame object inside the main() method.

    import javax.swing.*;
	public class FirstSwingExample {
	public static void main(String[] args) {
	JFrame f = new JFrame(); //Creating instance of JFrame
	JButton b = new JButton("Click"); //Creating instance of JButton
	b.setBounds(100, 100, 100, 100); //x-axis, y-axis, width, height
	f.add(b); //Adding button in JFrame
	f.setSize(500, 500); //width, height
	f.setLayout(null); //Using no layout managers
	f.setVisible(true); //Making the frame visible
	}
	}

Swing example using inheritance

	import javax.swing.*;
	public class SecondSwingExample extends JFrame { // Inheriting JFrame
	JFrame f;
	SecondSwingExample() {
	JButton b = new JButton("Click"); //Creating instance of JButton
	b.setBounds(100, 100, 100, 100); //x-axis, y-axis, width, height
	add(b); //Adding button on frame
	setSize(500, 500);
	setLayout(null);
	setVisible(true);
	}
	public static void main(String[] args) {
	new SecondSwingExample();
	}
	}

### Displaying Information in a Component
