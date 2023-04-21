import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class BotonRGB extends JFrame implements ActionListener{

  private JLabel label1, label2, label3;
  private JComboBox combo1, combo2, combo3;
  private JButton button1;


 public BotonRGB(){

  setLayout(null);

  label1 = new JLabel("Rojo:");
  label1.setBounds(10,15,100,15);
  add(label1);

  combo1 = new JComboBox();
  combo1.setBounds(120,10,50,30);
  for(int i = 0; i<=255; i++){
   combo1.addItem(String.valueOf(i));
  }
  add(combo1);

  label2 = new JLabel("Verde:");
  label2.setBounds(10,55,100,15);
  add(label2);

  combo2 = new JComboBox();
  combo2.setBounds(120,50,50,30);
  for(int i = 0; i<=255; i++){
   combo2.addItem(String.valueOf(i));
  }
  add(combo2);

  label3 = new JLabel("Azul:");
  label3.setBounds(10,95,100,15);
  add(label3);

  combo3 = new JComboBox();
  combo3.setBounds(120,90,50,30);
  for(int i = 0; i<=255; i++){
   combo3.addItem(String.valueOf(i));
  }
  add(combo3);

  button1 = new JButton("Aplicar");
  button1.setBounds(10,130,100,30);
  button1.addActionListener(this);
  add(button1);
 }


 public void actionPerformed(ActionEvent e){

  if(e.getSource() == button1){
   
   String palabra1 = combo1.getSelectedItem().toString();
   String palabra2 = combo2.getSelectedItem().toString();
   String palabra3 = combo3.getSelectedItem().toString();

   int rojo = Integer.parseInt(palabra1);
   int verde = Integer.parseInt(palabra2);
   int azul = Integer.parseInt(palabra3);

   Color color1 = new Color(rojo,verde,azul);
   button1.setBackground(color1);
  }
 }


 public static void main(String args[]){

  BotonRGB interfaz = new BotonRGB();
  interfaz.setBounds(0,0,200,220);
  interfaz.setVisible(true);
  interfaz.setResizable(false);
  interfaz.setLocationRelativeTo(null);
 }
}