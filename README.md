# Front-desk-application
import javax.swing.*;    
import java.awt.event.*;  
public class PProject {  
    public static void main(String[] args) {    
    JFrame myframe=new JFrame("log in");    
     final JLabel label = new JLabel();
     label.setBounds(20,150, 200,50); 
     
     final JPasswordField value = new JPasswordField();   
     value.setBounds(100,75,100,30);  
     
     JLabel name=new JLabel("username: ");    
        name.setBounds(20,20,80,30);
        
        JLabel pass=new JLabel("password: ");    
        pass.setBounds(20,75, 80,30);  
        
        JButton login = new JButton("log in");  
        login.setBounds(100,120, 80,30);
        
        final JTextField text = new JTextField();  
        text.setBounds(100,20, 100,30);    
                myframe.add(value); myframe.add(name); myframe.add(label); myframe.add(pass); myframe.add(login); myframe.add(text);  
                myframe.setSize(500,500);    
                myframe.setLayout(null);    
                myframe.setVisible(true);     
                login.addActionListener(new ActionListener() {  
                @Override
                public void actionPerformed(ActionEvent e) {       
                   String data = "username: " + text.getText();  
                   data += " password: "   
                   + new String(value.getPassword());   
                   label.setText(data);          
                }  
             });   
}  
}
