![image](https://github.com/user-attachments/assets/4e3fc516-22c9-4684-819a-1c93900bb97d)


# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

  -----------------------------------------------------------------------------------------------------------------------------------
  **Status**   **Name of Service**     **Screenshot**
  ------------ ----------------------- ----------------------------------------------------------------------------------------------
  Start        DevicePicker_73b520     ![image](https://github.com/user-attachments/assets/d017926a-c3dc-433a-ad6d-eacd97290173)

                                       

  Stop         DevicePicker_73b520     ![image](https://github.com/user-attachments/assets/23f66f25-8c3d-4335-af0d-88f75bbb82a2)


  Restart      DevicePicker_73b520     ![image](https://github.com/user-attachments/assets/35d6a2b0-73e2-4b47-9949-2c009291fca8)


  Pause        Intel(R) Graphics       ![image](https://github.com/user-attachments/assets/5a4fd95e-c46c-499b-837d-1a5d8304baf1)

  -----------------------------------------------------------------------------------------------------------------------------------

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
> ![image](https://github.com/user-attachments/assets/0292b31f-a558-4da3-802f-878f1666d828)
> ![image](https://github.com/user-attachments/assets/82cc2804-30ef-41ed-a47f-c70417b7c86b)
> ![image](https://github.com/user-attachments/assets/366b9aa2-c3b3-48ae-b439-e05edfd1fe3a)




5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![image](https://github.com/user-attachments/assets/d5e35d1d-8735-48e0-ad10-6f246acfcd48)


7.  Save the batch file in Z:\\lastname_timer.bat

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
>
> ![image](https://github.com/user-attachments/assets/29c32cd9-8766-421c-baf7-05fc562a9b42)



10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
> ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image13.png){width="4.625645231846019in"
> height="2.4170034995625547in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **/50**                                            
  ---------------------------------------------------------------------------------------
