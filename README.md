# class-12-java-project
class 12 grade informatics project
import  javax.swing.JOptionPane;
import  java.sql.*;
import  javax.swing.table.DefaultTableModel;

public class BEAUTYSHIELD extends javax.swing.JFrame {
DefaultTableModel tm;
Connection con;
Statement stmt;
ResultSet rs;
String c,nm,z;
float a,t,k;
int b ;
private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
logindlg.setVisible(true);// TODO add your handling code here:
    }                                        

    private void loginbtnActionPerformed(java.awt.event.ActionEvent evt) {                                         
String u=utf.getText();
String p=new String(ppf.getPassword());
if(u.equals("userid@gmail.com"))
{
    if(p.equals("marvel"))
    {
        JOptionPane.showMessageDialog(null,"WELCOME TO THE WORLD OF BEAUTY");
        HOME.setVisible(true);
    }
    else
    {
        JOptionPane.showMessageDialog(null,"OOPS...ITS SEEM THAT YOU HAE GOT AN ERROR");
        ppf.setText("");
        ppf.requestFocus();
    }
}
else
{
    JOptionPane.showMessageDialog(null,"ERROR USERNAME...TRY AGAIN");
    utf.setText("");
    utf.requestFocus();
}
// TODO add your handling code here:
    }                                        

    private void jLabel3MousePressed(java.awt.event.MouseEvent evt) {                                     
dressdlg.setVisible(true);// TODO add your handling code here:
    }                                    

    private void jLabel4MousePressed(java.awt.event.MouseEvent evt) {                                     
acdlg.setVisible(true);// TODO add your handling code here:
    }                                    

    private void jLabel5MousePressed(java.awt.event.MouseEvent evt) {                                     
mdlg.setVisible(true);// TODO add your handling code here:
    }                                    

    private void jLabel6MousePressed(java.awt.event.MouseEvent evt) {                                     
hdlg.setVisible(true);       // TODO add your handling code here:
    }                                    

    private void jLabel7MousePressed(java.awt.event.MouseEvent evt) {                                     
bdlg.setVisible(true);        // TODO add your handling code here:
    }                                    

    private void jLabel8MousePressed(java.awt.event.MouseEvent evt) {                                     
sdlg.setVisible(true);        // TODO add your handling code here:
    }                                    

    private void bluetopMousePressed(java.awt.event.MouseEvent evt) {                                     
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='bluetop';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}// TODO add your handling code here:
    }                                    

    private void jLabel68MousePressed(java.awt.event.MouseEvent evt) {                                      
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                     

    private void jLabel11MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='pinktop';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";    
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel12MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='captop';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel14MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='black jeans';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel15MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='silk saree';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel16MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='leatherjacket';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel17MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='gown';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel18MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='pallasso';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel19MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='coldshoulder';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel20MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='rippedjeans';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel21MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='scratchjeans';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel22MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='microjeans';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel24MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='frock';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel23MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='tshirt';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel30MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='pyjama';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel31MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='jutesilk';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel32MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='lehanga';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel29MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='kurti';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel27MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='bluekurti';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel69MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='blackjumpsuit';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
    }                                     

    private void jLabel33MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='redjumpsuit';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel51MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='crystalearring';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel57MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='goldchain';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel58MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='diamondring';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel60MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='blackwatch';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
    }                                     

    private void jLabel61MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='bangles';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel10MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='bracelet';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel44MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='shampoo';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel48MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='straightner';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel45MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='hairdryer';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel49MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='hairgel';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel46MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='hairoil';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel50MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='haircolor';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel47MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='hairspray';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel34MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='facecream';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel43MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='bodylotion';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel55MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='sunscreen';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel52MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='facewash';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel56MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='facebleach';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel53MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='facescrub';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel54MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='facepack';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel62MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='sportsshoe';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel63MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='highheels';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel64MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='flipflops';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel65MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='sandals';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel66MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='sneakers';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void jLabel67MousePressed(java.awt.event.MouseEvent evt) {                                      
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='boots';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                     

    private void rembtnActionPerformed(java.awt.event.ActionEvent evt) {                                       
String itnm=(JOptionPane.showInputDialog("Enter itname"));
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems where itname='"+itnm+"';";
    stmt=con.createStatement();
    stmt.executeUpdate(q);
    JOptionPane.showMessageDialog(null,"Record successfully removed");
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.setRowCount(0);
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from billitems;";
    Statement stmt=con.createStatement();
    ResultSet rs=stmt.executeQuery(q);
    while(rs.next())
    {
        String n=rs.getString("itname");
        int k=rs.getInt("itprice");
        int j=rs.getInt("quantity");
        String h=rs.getString("company");
        float f=rs.getFloat("total");
        Object ob[]={n,k,j,h,f};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}// TODO add your handling code here:
    }                                      

    private void jLabel59MousePressed(java.awt.event.MouseEvent evt) {                                      
paydlg.setVisible(true);        // TODO add your handling code here:
    }                                     

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
int s=0;
try
{
    Class.forName("java.sql.Driver");
    Connection con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    Statement stmt=con.createStatement();
    ResultSet rs=stmt.executeQuery("select sum(total) from billitems;");
    while(rs.next())
    {
    s=rs.getInt("sum(total)");
    slbl.setText(""+s);
    }
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
if(csrb.isSelected())
    JOptionPane.showMessageDialog(null,"Cash on Delivery on RS."+s);
if(crrb.isSelected())
    JOptionPane.showMessageDialog(null,"Credit Card Transaction on RS."+s);
if(drb.isSelected())
    JOptionPane.showMessageDialog(null,"Debit Card Transaction on RS."+s);
thankyoudlg.setVisible(true);// TODO add your handling code here:
    }                                        

    private void totbtnActionPerformed(java.awt.event.ActionEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
int h=0;
try
{
    Class.forName("java.sql.Driver");
    Connection con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    Statement stmt=con.createStatement();
    ResultSet rs=stmt.executeQuery("select sum(total) from billitems;");
    while(rs.next())
    {
    h=rs.getInt("sum(total)");
    slbl.setText(""+h);
    }
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}// TODO add your handling code here:
    }                                      

    private void okbtnActionPerformed(java.awt.event.ActionEvent evt) {                                      
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);    
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
System.exit(0);// TODO add your handling code here:
    }                                     

    private void jLabel86MousePressed(java.awt.event.MouseEvent evt) {                                      
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);    
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                     

    private void jLabel70MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='mascara';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel42MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='kajal';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel41MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='redlipliner';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel40MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='blush';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel39MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='compact';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel38MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='eyeshadow';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel37MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='pinklipgloss';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel36MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='blackeyeliner';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel35MousePressed(java.awt.event.MouseEvent evt) {                                      
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='redlipstick';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                     

    private void jLabel9MousePressed(java.awt.event.MouseEvent evt) {                                     
        tm=(DefaultTableModel)carttbl.getModel();
        try{
            Class.forName("java.sql.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            String q="select * from items where itname='foundation';";
            stmt=con.createStatement();
            rs=stmt.executeQuery(q);
            while(rs.next()) {
                nm=rs.getString("itname");
                a=rs.getFloat("itprice");
                b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
                t=a*b;
                c=rs.getString("company");
                Object ob[]={nm,a,c,b,t};
                tm.addRow(ob);
            }
            rs.close();
            stmt.close();
            con.close();
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }
        try{
            Class.forName("com.mysql.jdbc.Driver");
            con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
            stmt=con.createStatement();
            String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
            stmt.executeUpdate(z);
            JOptionPane.showMessageDialog(null,"Added successfully");
        } catch(Exception e) {
            JOptionPane.showMessageDialog(null,e.getMessage());
        }        // TODO add your handling code here:
}                                    

    private void jLabel139MousePressed(java.awt.event.MouseEvent evt) {                                       
dressdlg.dispose();// TODO add your handling code here:
    }                                      

    private void jLabel140MousePressed(java.awt.event.MouseEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);    
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
dressdlg.dispose();
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                      

    private void jLabel141MousePressed(java.awt.event.MouseEvent evt) {                                       
dressdlg.dispose();
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                      

    private void jLabel112MousePressed(java.awt.event.MouseEvent evt) {                                       
mdlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel110MousePressed(java.awt.event.MouseEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
mdlg.dispose();
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                      

    private void jLabel111MousePressed(java.awt.event.MouseEvent evt) {                                       
mdlg.dispose();
cartdlg.setVisible(true);// TODO add your handling code here:
    }                                      

    private void jLabel138MousePressed(java.awt.event.MouseEvent evt) {                                       
acdlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel147MousePressed(java.awt.event.MouseEvent evt) {                                       
hdlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel156MousePressed(java.awt.event.MouseEvent evt) {                                       
bdlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel152MousePressed(java.awt.event.MouseEvent evt) {                                       
sdlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel159MousePressed(java.awt.event.MouseEvent evt) {                                       
cartdlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel104MousePressed(java.awt.event.MouseEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
acdlg.dispose();
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                      

    private void jLabel105MousePressed(java.awt.event.MouseEvent evt) {                                       
acdlg.dispose();
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                      

    private void jLabel148MousePressed(java.awt.event.MouseEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
hdlg.dispose();
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                      

    private void jLabel155MousePressed(java.awt.event.MouseEvent evt) {                                       
hdlg.dispose();
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                      

    private void jLabel157MousePressed(java.awt.event.MouseEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);    
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
bdlg.dispose();
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                      

    private void jLabel158MousePressed(java.awt.event.MouseEvent evt) {                                       
bdlg.dispose();
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                      

    private void jLabel153MousePressed(java.awt.event.MouseEvent evt) {                                       
sdlg.dispose();
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                      

    private void jLabel151MousePressed(java.awt.event.MouseEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
sdlg.dispose();
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                      

    private void jLabel160MousePressed(java.awt.event.MouseEvent evt) {                                       
DefaultTableModel tm=(DefaultTableModel)carttbl.getModel();
try
{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="delete from billitems;";
    stmt=con.createStatement();
    stmt.executeUpdate(q);
    rs.close();
    stmt.close();
    con.close();
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
tm.removeRow(0);
cartdlg.dispose();
HOME.dispose();
logindlg.dispose();
utf.setText("");
ppf.setText("");// TODO add your handling code here:
    }                                      

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
dressdlg2.setVisible(true);        // TODO add your handling code here:
    }                                        

    private void jButton4ActionPerformed(java.awt.event.ActionEvent evt) {                                         
dressdlg2.dispose();        // TODO add your handling code here:
    }                                        

    private void jLabel264MousePressed(java.awt.event.MouseEvent evt) {                                       
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='croptop';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                      

    private void jLabel265MousePressed(java.awt.event.MouseEvent evt) {                                       
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='pinkkurti';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                      

    private void jLabel266MousePressed(java.awt.event.MouseEvent evt) {                                       
tm=(DefaultTableModel)carttbl.getModel();
try{
    Class.forName("java.sql.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    String q="select * from items where itname='jacket';";
    stmt=con.createStatement();
    rs=stmt.executeQuery(q);
    while(rs.next())
    {
        nm=rs.getString("itname");
        a=rs.getFloat("itprice");
        b=Integer.parseInt(JOptionPane.showInputDialog("Enter Quantity"));
        t=a*b;
        c=rs.getString("company");
        Object ob[]={nm,a,c,b,t};
        tm.addRow(ob);
    }
    rs.close();
    stmt.close();
    con.close();
    }
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}
try{
    Class.forName("com.mysql.jdbc.Driver");
    con=DriverManager.getConnection("jdbc:mysql://localhost/beautyshield","root","sms");
    stmt=con.createStatement();
    String z="insert into billitems values('"+nm+"','"+a+"','"+b+"','"+c+"','"+t+"');";
    stmt.executeUpdate(z);
    JOptionPane.showMessageDialog(null,"Added successfully");
}
catch(Exception e)
{
    JOptionPane.showMessageDialog(null,e.getMessage());
}        // TODO add your handling code here:
    }                                      

    private void jButton5ActionPerformed(java.awt.event.ActionEvent evt) {                                         
dressdlg3.setVisible(true);        // TODO add your handling code here:
    }                                        

    private void jLabel185MousePressed(java.awt.event.MouseEvent evt) {                                       
dressdlg2.dispose();
dressdlg.dispose();       // TODO add your handling code here:
    }                                      

    private void jLabel28MousePressed(java.awt.event.MouseEvent evt) {                                      
dressdlg3.dispose();
dressdlg2.dispose();
dressdlg.dispose();// TODO add your handling code here:
    }                                     

    private void jLabel186MousePressed(java.awt.event.MouseEvent evt) {                                       
utf.setText("");
ppf.setText("");
dressdlg2.dispose();
dressdlg.dispose();
HOME.dispose();
logindlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel254MousePressed(java.awt.event.MouseEvent evt) {                                       
utf.setText("");
ppf.setText("");
dressdlg3.dispose();
dressdlg2.dispose();
dressdlg.dispose();
HOME.dispose();
logindlg.dispose();        // TODO add your handling code here:
    }                                      

    private void jLabel187MousePressed(java.awt.event.MouseEvent evt) {                                       
dressdlg2.dispose();
dressdlg.dispose();
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                      

    private void jLabel256MousePressed(java.awt.event.MouseEvent evt) {                                       
dressdlg3.dispose();
dressdlg2.dispose();
dressdlg.dispose();
cartdlg.setVisible(true);        // TODO add your handling code here:
    }                                      

    private void jButton6ActionPerformed(java.awt.event.ActionEvent evt) {                                         
dressdlg3.dispose();// TODO add your handling code here:
    }
