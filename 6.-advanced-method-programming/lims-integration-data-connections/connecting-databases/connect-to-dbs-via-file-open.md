# Connect to DBs via File:Open

<figure><img src="../../../.gitbook/assets/image (439).png" alt=""><figcaption></figcaption></figure>

What is a Connection String?

* String of attributes needed to connect to a database
*   Consists of key-value pairs separated by a “;” and passed to a provider

    Provider?
*   A provider is a software component that your application (ex. Hamilton method) uses to interact directly with your data source.

    What does the connection string require?
* Data source (SQL Server, Oracle, MySQL, PostgreSQL, etc.)
* Data provider (SQLOLEDB, MyOracleDB)
* Security Options (Use username/password or Windows Authentication)
  *   Standard Security

      ```plaintext
      Provider=sqloledb; Data Source=myServerAddress; Initial Catalog=myDataBase; 
      User Id=myUsername; Password=myPassword;
      ```

      ***
  *   Trusted Connection

      ```plaintext
      Provider=sqloledb; Data Source=myServerAddress; Initial Catalog=myDataBase; 
      Integrated Security=SSPI;
      ```



For more information, visit [www.connectionstrings.com](https://www.connectionstrings.com)
