package gui;

import javax.swing.JFrame;
import javax.swing.JPanel;

import logic.MainController;

public class MainFrame extends JFrame {

	private JPanel contentPane;

	/**
	 * Create the frame.
	 * 
	 * @param mainController
	 */
	MainController mainController;

	public MainFrame(MainController mc) {
		this.mainController = mc;
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setMinimumSize(new java.awt.Dimension(950, 500));
		setResizable(false);
	}

	public void setPanel(JPanel jp) {
		this.getContentPane().removeAll();
		this.getContentPane().add(jp);
		setVisible(true);
		repaint();
	}

}
