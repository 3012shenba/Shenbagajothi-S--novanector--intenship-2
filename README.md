package application;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;



import javax.swing.BoxLayout;

import javax.swing.ButtonGroup;

import javax.swing.JButton;

import javax.swing.JFrame;

import javax.swing.JLabel;

import javax.swing.JOptionPane;

import javax.swing.JPanel;

import javax.swing.JPasswordField;

import javax.swing.JRadioButton;

import javax.swing.JTextField;

import javax.swing.SwingUtilities;



import javax.swing.*;

import java.awt.*;

import java.awt.event.*;



import javax.swing.*;

import java.awt.*;

import java.awt.event.*;

import javax.swing.*;

import java.awt.*;



@SuppressWarnings("unused")

public class PortfolioApp {



    public static void main(String[] args) {

        // Create the main frame

        JFrame frame = new JFrame("My Portfolio");

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        frame.setSize(800, 600);

        frame.setLocationRelativeTo(null); // Center the frame



        // Create a panel for the header

        JPanel headerPanel = new JPanel();

        headerPanel.setBackground(new Color(70, 130, 180)); // Steel Blue color

        headerPanel.setPreferredSize(new Dimension(800, 100));



        JLabel headerLabel = new JLabel("My Portfolio");

        headerLabel.setFont(new Font("Arial", Font.BOLD, 36));

        headerLabel.setForeground(Color.WHITE);

        headerPanel.add(headerLabel);



        // Create a panel for the content

        JPanel contentPanel = new JPanel();

        contentPanel.setLayout(new GridLayout(3, 1)); // 3 rows, 1 column



        // Add content sections

        contentPanel.add(createContentSection("About Me", "This is a brief introduction about myself."));

        contentPanel.add(createContentSection("Projects", "Project 1\nProject 2\nProject 3"));

        contentPanel.add(createContentSection("Skills", "Java, Python, HTML, CSS, JavaScript"));



        // Add panels to the frame

        frame.getContentPane().add(headerPanel, BorderLayout.NORTH);

        frame.getContentPane().add(contentPanel, BorderLayout.CENTER);



        // Make the frame visible

        frame.setVisible(true);

    }



    private static JPanel createContentSection(String title, String content) {

        JPanel panel = new JPanel();

        panel.setBorder(BorderFactory.createTitledBorder(title));

        panel.setLayout(new BorderLayout());



        JTextArea textArea = new JTextArea(content);

        textArea.setLineWrap(true);

        textArea.setWrapStyleWord(true);

        textArea.setEditable(false);



        JScrollPane scrollPane = new JScrollPane(textArea);

        panel.add(scrollPane, BorderLayout.CENTER);



        return panel;

    }

}

