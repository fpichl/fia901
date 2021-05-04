=====================
Anwendungsentwicklung
=====================

Unterrichtet von Herrn Katzberg

#####################
MSSQL Server Anbindung in Java
#####################

.. code-block:: java

 import java.sql.*;

 public class MSSQL_Java {
    public static void main(String[]  args) throws ClassNotFoundException {

        Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");

        String connectionURL = "jdbc:sqlserver://localhost:1434;databaseName=TestDB;integratedSecurity=true;";

        try(Connection connection = DriverManager.getConnection(connectionURL)) {

            Statement statement = connection.createStatement();

            String sql = "SELECT * FROM dbo.T_PERSON";
            ResultSet resultSet = statement.executeQuery(sql);

            while(resultSet.next()) {
                System.out.println(resultSet.getString("NAME") + " : " + resultSet.getString("Nachname"));
            }

        } catch (SQLException throwable) {
            throwable.printStackTrace();
        }
    }
 }
..
