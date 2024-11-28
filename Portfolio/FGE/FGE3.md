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
  Start        DevicePicker_73b520     ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image2.png){width="2.229478346456693in"
                                       height="1.9690244969378827in"}

                                       

  Stop         DevicePicker_73b520     ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image3.png){width="2.1982239720034995in"
                                       height="1.9794433508311462in"}

  Restart      DevicePicker_73b520     ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image4.png){width="3.4242038495188103in"
                                       height="1.7038888888888888in"}

  Pause        Intel(R) Graphics       ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image5.png){width="3.4293832020997375in"
               Command Center Service  height="3.4226443569553804in"}
  -----------------------------------------------------------------------------------------------------------------------------------

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
>
> ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image6.png){width="2.4652121609798776in"
> height="2.2741108923884514in"}![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image7.png){width="2.72123031496063in"
> height="2.2584831583552054in"}
>
> ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image8.png){width="3.3773589238845143in"
> height="3.0499628171478563in"}![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image9.png){width="3.0593536745406826in"
> height="2.9475240594925634in"}
>
> ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image10.png){width="4.188083989501313in"
> height="3.7401049868766405in"}

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image11.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

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
> ![](vertopal_3b94e4f869f24359b97230b6a4948f0e/media/image12.png){width="5.365332458442695in"
> height="0.3646347331583552in"}

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
