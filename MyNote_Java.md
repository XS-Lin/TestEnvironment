# メモ #

## OJDBC ##

引用元 [Oracle JDBC FAQ](https://www.oracle.com/technetwork/jp/database/application-development/jdbc/overview/default-090281-ja.html#01_01)

1. Oracle JDBCのリリースとJDKのバージョン

   |Oracle Databaseのバージョン|リリース固有のJDBC jarファイル|
   |---|---|
   |18.3|ojdbc8.jar（JDK 8、JDK 9、JDK 10およびJDK 11）|
   |12.2または12c R2|ojdbc8.jar（JDK 8）|
   |12.1または12c R1|ojdbc7.jar（JDK 7およびJDK 8） ojdbc6.jar（JDK 6)|
   |11.2または11g R2|ojdbc6.jar（JDK 6、JDK 7、およびJDK 8）**（注：JDK 7とJDK 8は、11.2.0.3と11.2.0.4のみでサポートされます）** ojdbc5.jar（JDK 5）|

1. Oracle DBバージョンのクライアント/サーバー相互運用性マトリックスまたは認定マトリックス

   | 相互運用性マトリックス | Database 18.3 | Database 12.2および12.1 | Database 11.2.0.x |
   |---|---|---|---|
   | JDBC 18.3 | 対応 | 対応 | 対応 |
   | JDBC 12.2および12.1 | 対応 | 対応 | 対応 |
   | JDBC 11.2.0.x | 対応 | 対応 | 対応 |

1. Oracle JDBCのリリースとJDBCの仕様の関連

   | Oracle Databaseのバージョン | JDBC仕様の準拠 |
   |---|---|
   | 18.3 | ojdbc8.jarのJDBC 4.2 |
   | 12.2または12c R2 | ojdbc8.jarのJDBC 4.2 |
   | 12.1または12c R1 | ojdbc7.jarのJDBC 4.1、ojdbc6.jarのJDBC 4.0 |
   | 11.2または11g R2 | ojdbc6.jarのJDBC 4.0、ojdbc5.jarのJDBC 3.0 |

1. JDBC jarファイルはどこから入手できますか。

   必要なJDBC jarファイルは、Oracle Technology Networkの[SQLJ & JDBCダウンロード・ページ](https://www.oracle.com/database/technologies/appdev/jdbc-downloads.html)からダウンロードしてください。
