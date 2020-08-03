# utl-rename-variables-with-the-same-prefix-dosubl-varlist
Rename variables with the same prefix dosubl varlist
    Rename variables with the same prefix and arbitrary sufixes dosubl varlist                                   
                                                                                                                 
    github                                                                                                       
    https://tinyurl.com/y6bfsr7z                                                                                 
    https://github.com/rogerjdeangelis/utl-rename-variables-with-the-same-prefix-dosubl-varlist                  
                                                                                                                 
    SAS Forum                                                                                                    
    https://tinyurl.com/yxmz4x7t                                                                                 
    https://communities.sas.com/t5/SAS-Studio/Macro-to-rename-variables-with-the-same-prefix/m-p/673659          
                                                                                                                 
    Changing the prefix for 70 variables that do not have sequential sufixes.                                    
                                                                                                                 
    Substantial amouunt of the code is error checking.                                                           
                                                                                                                 
    AUTOMATE THESE RENAMES                                                                                       
                                                                                                                 
    RENAME (note inly the prefix is changed)                                                                     
                                                                                                                 
       MONTH_JAN10  = MTH_JAN10                                                                                  
       MONTH_FEB10  = MTH_FEB10                                                                                  
       MONTH_MAR10  = MTH_MAR10                                                                                  
       MONTH_APR10  = MTH_APR10                                                                                  
       MONTH_MAY10  = MTH_MAY10                                                                                  
       MONTH_JUN10  = MTH_JUN10                                                                                  
                                                                                                                 
       PAY_110      = SALARY_110                                                                                 
       PAY_210      = SALARY_210                                                                                 
       PAY_310      = SALARY_310                                                                                 
       PAY_410      = SALARY_410                                                                                 
       PAY_510      = SALARY_510                                                                                 
       PAY_610      = SALARY_610                                                                                 
                                                                                                                 
    /*                   _                                                                                       
    (_)_ __  _ __  _   _| |_                                                                                     
    | | `_ \| `_ \| | | | __|                                                                                    
    | | | | | |_) | |_| | |_                                                                                     
    |_|_| |_| .__/ \__,_|\__|                                                                                    
            |_|                                                                                                  
    */                                                                                                           
                                                                                                                 
    data have;                                                                                                   
                                                                                                                 
      retain                                                                                                     
         MONTH_JAN10                                                                                             
         MONTH_FEB10                                                                                             
         MONTH_MAR10                                                                                             
         MONTH_APR10                                                                                             
         MONTH_MAY10                                                                                             
         MONTH_JUN10                                                                                             
         PAY_110                                                                                                 
         PAY_210                                                                                                 
         PAY_310                                                                                                 
         PAY_410                                                                                                 
         PAY_510                                                                                                 
         PAY_610                                                                                                 
         0                                                                                                       
    ;                                                                                                            
    run;quit;                                                                                                    
                                                                                                                 
                                                                                                                 
    Middle Observation(1 ) of Last dataset = WORK.HAVE - Total Obs 1                                             
                                                                                                                 
     -- NUMERIC --                                                                                               
                                                                                                                 
    VARIABLE                                                                                                     
                                                                                                                 
    MONTH_JAN10       N8       0                                                                                 
    MONTH_FEB10       N8       0                                                                                 
    MONTH_MAR10       N8       0                                                                                 
    MONTH_APR10       N8       0                                                                                 
    MONTH_MAY10       N8       0                                                                                 
    MONTH_JUN10       N8       0                                                                                 
    PAY_110           N8       0                                                                                 
    PAY_210           N8       0                                                                                 
    PAY_310           N8       0                                                                                 
    PAY_410           N8       0                                                                                 
    PAY_510           N8       0                                                                                 
    PAY_610           N8       0                                                                                 
                                                                                                                 
                                                                                                                 
    /*           _               _                                                                               
      ___  _   _| |_ _ __  _   _| |_                                                                             
     / _ \| | | | __| `_ \| | | | __|                                                                            
    | (_) | |_| | |_| |_) | |_| | |_                                                                             
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                            
                    |_|                                                                                          
    */                                                                                                           
                                                                                                                 
    DOSUBL PROVIDES LOGGING                                                                                      
                                                                                                                 
    WORK.LOG total obs=12                                                                                        
                                                                                                                 
     VAR            NEWPFX                       STATUS                                                          
                                                                                                                 
     PAY_110        SALARY      prefix of PAY_110 changed to SALARY                                              
     PAY_210        SALARY      prefix of PAY_210 changed to SALARY                                              
     PAY_310        SALARY      prefix of PAY_310 changed to SALARY                                              
     PAY_410        SALARY      prefix of PAY_410 changed to SALARY                                              
     PAY_510        SALARY      prefix of PAY_510 changed to SALARY                                              
     PAY_610        SALARY      prefix of PAY_610 changed to SALARY                                              
                                                                                                                 
     MONTH_JAN10    MTH         prefix of MONTH_JAN10 changed to MTH                                             
     MONTH_FEB10    MTH         prefix of MONTH_FEB10 changed to MTH                                             
     MONTH_MAR10    MTH         prefix of MONTH_MAR10 changed to MTH                                             
     MONTH_APR10    MTH         prefix of MONTH_APR10 changed to MTH                                             
     MONTH_MAY10    MTH         prefix of MONTH_MAY10 changed to MTH                                             
     MONTH_JUN10    MTH         prefix of MONTH_JUN10 changed to MTH                                             
                                                                                                                 
                                                                                                                 
    NOTE THE PREFIX HAS BEEN CHANGED                                                                             
    =================================                                                                            
                                                                                                                 
    Middle Observation(1 ) of have - Total Obs 1                                                                 
                                                                                                                 
     -- NUMERIC --                                                                                               
    MTH_JAN10           N8       0                                                                               
    MTH_FEB10           N8       0                                                                               
    MTH_MAR10           N8       0                                                                               
    MTH_APR10           N8       0                                                                               
    MTH_MAY10           N8       0                                                                               
    MTH_JUN10           N8       0                                                                               
                                                                                                                 
    SALARY_110          N8       0                                                                               
    SALARY_210          N8       0                                                                               
    SALARY_310          N8       0                                                                               
    SALARY_410          N8       0                                                                               
    SALARY_510          N8       0                                                                               
    SALARY_610          N8       0                                                                               
                                                                                                                 
    /*                                                                                                           
     _ __  _ __ ___   ___ ___  ___ ___                                                                           
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|                                                                          
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                          
    | .__/|_|  \___/ \___\___||___/___/                                                                          
    |_|                                                                                                          
    */                                                                                                           
                                                                                                                 
    data have;                                                                                                   
                                                                                                                 
      retain                                                                                                     
         MONTH_JAN10                                                                                             
         MONTH_FEB10                                                                                             
         MONTH_MAR10                                                                                             
         MONTH_APR10                                                                                             
         MONTH_MAY10                                                                                             
         MONTH_JUN10                                                                                             
         PAY_110                                                                                                 
         PAY_210                                                                                                 
         PAY_310                                                                                                 
         PAY_410                                                                                                 
         PAY_510                                                                                                 
         PAY_610                                                                                                 
         0                                                                                                       
    ;                                                                                                            
    run;quit;                                                                                                    
                                                                                                                 
    %symdel var sfx newpfx cc / nowarn;                                                                          
                                                                                                                 
    data log;                                                                                                    
                                                                                                                 
        length var $16;                                                                                          
                                                                                                                 
        do var=                                                                                                  
           %unquote(%varlist(have,qstyle=Oracle,od=%str(,),prx=/PAY/i))                                          
           ,%unquote(%varlist(have,qstyle=Oracle,od=%str(,),prx=/MONTH/i));                                      
                                                                                                                 
           select (scan(var,1,"_"));                                                                             
              when("MONTH") newPfx ="MTH   ";                                                                    
              when("PAY"  ) newPfx= "SALARY";                                                                    
           end;                                                                                                  
                                                                                                                 
           call symputx('var',var);                                                                              
           call symputx('sfx',scan(var,2,"_"));                                                                  
           call symputx('newpfx',newpfx);                                                                        
                                                                                                                 
             rc=dosubl('                                                                                         
                proc datasets lib=work nolist;                                                                   
                   modify have;                                                                                  
                      rename                                                                                     
                        &var = &newPfx._&sfx                                                                     
                ;run;quit;                                                                                       
                %let cc=&syserr;                                                                                 
             ');                                                                                                 
           if symgetn("cc")=0 then status=catx(' ','prefix of',var,'changed to',newPfx);                         
           else status=catx(' ','prefix of',var,'NOT changed to',newPfx);                                        
           output;                                                                                               
        end;                                                                                                     
                                                                                                                 
        drop rc;                                                                                                 
        stop;                                                                                                    
                                                                                                                 
    run;quit;                                                                                                    
                                                                                                                 
