import javax.swing.*;
import java.awt.event.*;

public class Interfaz extends JFrame implements ActionListener{

  private JTextField textfield1;
  private JTextArea textarea1;
  private JScrollPane scrollpane1;
  private JButton boton1;
  String texto = "";


 public Interfaz(){

  setLayout(null);
  textfield1 = new JTextField();
  textfield1.setBounds(10,10,200,30);
  add(textfield1);

  textarea1 = new JTextArea();
  scrollpane1 = new JScrollPane(textarea1);
  scrollpane1.setBounds(10,50,400,300);
  add(scrollpane1);

  boton1 = new JButton("Agregar");
  boton1.setBounds(250,10,100,30);
  add(boton1);
  boton1.addActionListener(this);
 }


 public void actionPerformed(ActionEvent e){

  if(e.getSource() == boton1){
   texto += textfield1.getText() + "\n";
   textarea1.setText(texto);
   textfield1.setText("");
  }
 }


 public static void main(String args[]){

  Interfaz interfaz1 = new Interfaz();
  interfaz1.setBounds(0,0,540,400);
  interfaz1.setVisible(true);
  interfaz1.setResizable(false);
  interfaz1.setLocationRelativeTo(null);
 }
}