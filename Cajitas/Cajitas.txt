import javax.swing.*;
import javax.swing.event.*;

public class Cajitas extends JFrame implements ChangeListener{

  private JCheckBox check1, check2, check3;
  

 public Cajitas(){

  setLayout(null);

  check1 = new JCheckBox("Inglés");
  check1.setBounds(10,10,150,30);
  check1.addChangeListener(this);  
  add(check1);

  check2 = new JCheckBox("Francés");
  check2.setBounds(10,50,150,30);
  check2.addChangeListener(this);
  add(check2);

  check3 = new JCheckBox("Alemán");
  check3.setBounds(10,90,150,30);
  check3.addChangeListener(this);
  add(check3);
 }


 public void stateChanged(ChangeEvent e){

  String cadena = "";

  if(check1.isSelected() == true){
   cadena = cadena + "-Inglés-"; 
  }

  if(check2.isSelected() == true){
   cadena = cadena + "-Francés-";
  }

  if(check3.isSelected() == true){
   cadena = cadena + "-Alemán-";
  }

  setTitle(cadena);
 }


 public static void main(String args[]){

  Cajitas interfaz = new Cajitas();
  interfaz.setBounds(0,0,350,200);
  interfaz.setVisible(true);
  interfaz.setResizable(false);
  interfaz.setLocationRelativeTo(null);
 }
}