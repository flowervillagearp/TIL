# ERROR: connect ECONNREFUSED ::1:3306

Your connection attempt failed for user 'root' to the MySQL server at localhost:3306:
Access denied for user 'root'@'localhost' (using password: YES)

Please:
1 Check that MySQL is running on address localhost
2 Check that MySQL is reachable on port 3306 (note: 3306 is the default, but this can be changed)
3 Check the user root has rights to connect to localhost from your address (MySQL rights define what clients can connect to the server and from which machines) 
4 Make sure you are both providing a password if needed and using the correct password for localhost connecting from the host address you're connecting from



* node버전 확인해보기

    원인이 무었인지는 모르겠지만 node버전을 lts로 바꿔서 해결되었음