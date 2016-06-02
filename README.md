# PHPLogger
Create Stat log in php Application 

#PHPLogger Example 

    require_once './PHPLogger.php';
    
    define('LOG_FILE', '/var/log/stat/');
    $logger = new PHPLogger(LOG_FILE);
    
    //attach 
    $dashboard_Access = new Reportlog('Dashboard_Access');
    $logger->attach($dashboard_Access);
    
    
    $password_Change = new Reportlog('password_Change');
    $logger->attach($password_Change);
    
    //fire event     
    $logger->writeLog();

