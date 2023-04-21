import javax.swing.*;
import java.awt.event.*;

public class Interfaz extends JFrame implements ItemListener{

  private JComboBox combobox1;


 public Interfaz(){

  setLayout(null);
  
  combobox1 = new JComboBox();
  combobox1.setBounds(10,10,80,20);
  add(combobox1);

  combobox1.addItem("rojo");
  combobox1.addItem("verde");
  combobox1.addItem("azul");
  combobox1.addItem("amarillo");
  combobox1.addItem("negro");
  
  combobox1.addItemListener(this);
 }


 public void itemStateChanged(ItemEvent e){

  if(e.getSource() == combobox1){
   String seleccion = combobox1.getSelectedItem().toString();
   setTitle(seleccion);
  }
 }  


 public static void main(String args[]){

  Interfaz interfaz1 = new Interfaz();
  interfaz1.setBounds(0,0,250,150);
  interfaz1.setVisible(true);
  interfaz1.setResizable(false);
  interfaz1.setLocationRelativeTo(null);
 }
}