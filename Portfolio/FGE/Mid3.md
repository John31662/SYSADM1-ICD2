![image](https://github.com/user-attachments/assets/5dff3ca1-f266-4852-8311-93e2f54042a7)


# SYSADM1 -- Platform Services

# Requirement: 

-   A virtual machine running Windows Server

    **Objective/s:**

    To analyze IIS logs in the Event Viewer to identify critical web
    service metrics, understand common error codes, and learn how to
    monitor the health of web applications.

**Instructions**

**Part 1: Opening Event Viewer and Loading Logs**

1.  Access the event viewer in the server.

2.  From the event viewer, explore the windows log and list down its
    major categories
    
![image](https://github.com/user-attachments/assets/cbbb6b40-62e3-448f-8580-1f38e772e7f4)


**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

> **Errors**

![image](https://github.com/user-attachments/assets/49989681-ef5f-424d-853d-62cce7cc2e1f)


**Warnings**

![image](https://github.com/user-attachments/assets/51bf52db-b137-4c12-bfc9-16a1d2aacc78)

2.  ![image](https://github.com/user-attachments/assets/261805f0-39c6-4aa2-b39e-af7cac33d007)


![image](https://github.com/user-attachments/assets/4ea1ebd9-f2e9-464f-bdae-381e9aec8183)


No critical errors but basing on the screenshot on item one the
recurring events would be event ID no. 1001 as basing it on the time
stamp. In addition the event ID 7023 also recurred two times. Onto the
warnings the most recurring warning was event ID no. 34 with the warning
event no. 5781 was also found.

[To sum it up there were 8 non critical errors and 6
warnings.]{.underline}

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

        -   **Event ID**

        -   **Source**

        -   **Timestamp**

        -   **Description**

EVENTS

+-------+---------+-----------+---------------------------------------+
| **    | **S     | **TIME    | **DESCRIPTION**                       |
| EVENT | OURCE** | STAMP**   |                                       |
| ID**  |         |           |                                       |
+=======+=========+===========+=======================================+
| 1001  | SceCli  | 1         | Security policy cannot be propagated. |
|       |         | 0/17/2024 | Cannot access the template. Error     |
|       |         | 9:17:09   | code = 3.                             |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 1001  | SceCli  | 1         | Security policy cannot be propagated. |
|       |         | 0/17/2024 | Cannot access the template. Error     |
|       |         | 9:17:09   | code = 3.                             |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 1001  | SceCli  | 1         | Security policy cannot be propagated. |
|       |         | 0/17/2024 | Cannot access the template. Error     |
|       |         | 9:17:07   | code = 3.                             |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 1001  | SceCli  | 1         | Security policy cannot be propagated. |
|       |         | 0/17/2024 | Cannot access the template. Error     |
|       |         | 9:17:07   | code = 3.                             |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 7023  | Service | 1         | The windows time service terminated   |
|       | Control | 0/17/2024 | with the following error:             |
|       | Manager | 9:13:06   |                                       |
|       |         | AM        | An attempt was made to logon, but the |
|       |         |           | network logon service was not         |
|       |         |           | started.                              |
+-------+---------+-----------+---------------------------------------+
| 7023  | Service | 1         | The windows time service terminated   |
|       | Control | 0/17/2024 | with the following error:             |
|       | Manager | 9:13:20   |                                       |
|       |         | AM        | An attempt was made to logon, but the |
|       |         |           | network logon service was not         |
|       |         |           | started.                              |
+-------+---------+-----------+---------------------------------------+
| 46    | Time-   | 1         | The time service encountered an error |
|       | Service | 0/17/2024 | and was forced to shut down. An       |
|       |         | 9:13:06   | attempt was made to logon, but the    |
|       |         | AM        | logon service was not started.        |
+-------+---------+-----------+---------------------------------------+
| 46    | Time-   | 1         | The time service encountered an error |
|       | Service | 0/17/2024 | and was forced to shut down. An       |
|       |         | 9:13:30   | attempt was made to logon, but the    |
|       |         | AM        | logon service was not started.        |
+-------+---------+-----------+---------------------------------------+
| 34    | disk    | 1         | The driver disabled the write cache   |
|       |         | 0/17/2024 | on device                             |
|       |         | 9:13:18   |                                       |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 34    | disk    | 1         | The driver disabled the write cache   |
|       |         | 0/17/2024 | on device                             |
|       |         | 9:13:18   |                                       |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 34    | disk    | 1         | The driver disabled the write cache   |
|       |         | 0/17/2024 | on device                             |
|       |         | 9:13:18   |                                       |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 34    | disk    | 1         | The driver disabled the write cache   |
|       |         | 0/17/2024 | on device                             |
|       |         | 9:13:30   |                                       |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 34    | disk    | 1         | The driver disabled the write cache   |
|       |         | 0/17/2024 | on device                             |
|       |         | 9:13:30   |                                       |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+
| 34    | disk    | 1         | The driver disabled the write cache   |
|       |         | 0/17/2024 | on device                             |
|       |         | 9:13:30   |                                       |
|       |         | AM        |                                       |
+-------+---------+-----------+---------------------------------------+

**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

> The most recurring errors I found was the errors from event ID no.
> 1001 and event ID no. 7023

2.  Is there a specific time or pattern to these errors?

From what I saw there was a pattern in the errors since it only happened
in a quick amount of time and happened a short while after, it must be
re trying to re connect to accomplish a task

3.  Draft a Troubleshooting Report:

    -   Based on the events found, create a short report with the
        following sections:

**Report Structure**

**1.** Overview

Based on my previous screenshots this report would be about errors logs
and what does it do when did it happen and why did it happen I will be
discussing my findings down below, with this in mind I will show what
errors I encountered during this activity and explain my key findings
and my possible solutions. I would also identify the root causes.

**2.** Key Findings

-   List the critical events you found. Example (no critical error found
    here normal errors instead):

    -   **Event ID 1001**: Security cannot be propagated and cannot
        access template at 9:17 AM

    -   **Event ID 46**: An attempt was made to logon but it was blocked
        at 9:13 AM

    -   **Event ID 34:** Drivers disabled with write cache on device
        around 9:13 AM

**3.** Root Causes and Solutions

**Event ID 1001** this can be caused by outdated drivers, overheating
and possible malware or virus attack and can cause system lookup
potentially leading a BSOD to find a solution for this error is to make
sure all your drivers are up to date and occasionally scan the computer
with windows defender to remove unwanted threats.

**Event ID 46:** this can be caused when a computer boots without a
configured dump file. To avoid this error is you must enable Memory dump
Settings this will resolve the issues.

**Event ID 34:** the possible cause of this is when a driver device is
not properly inputted into the system which causes an error causing the
device failing to load, to fix this as simple as unplugging and
reconnecting would mainly fix the errors.

**Part 4: Reflection Questions**

1.  Most recurring error

> My findings of the most recurring error would be the Event ID no. 1001

2.  How would you **monitor login attempts** to detect potential
    security threats?

> With the use of identity analytics took it can monitor patterns across
> systems as these tools can detect anomalies such as excessive login
> attempts that raises a red flag the used or abnormal file access can
> also raise a red flag with the use of identity analytics tool it can
> provide early warnings of potential breaches. With information an
> administrator can better be prepared for the future. You can also use
> third party applications to better improve findings in the system.

3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

> It is important to review your logs to make sure nothing wrong is
> happening behind the scenes of your computer, the monitoring logs can
> also help you detect potential problems that will arise in the future
> so you can find solutions to avoid problems that will occur in the
> future. I believe this is the importance of monitoring logs.

Grading Rubric

  ---------------------------------------------------------------------------------------------------------------------------------------
  **Criteria**        **Excellent**     **Good**          **Needs                           **Poor**                         **Points**
                                                          Improvement**                                                      
  ------------------- ----------------- ----------------- --------------- ----------------- ------------- ------------------ ------------
  **Log Analysis**    Identifies all    Identifies most   Identifies some                   Fails to                         /10
                      key events (503,  key events with   events, but                       identify key                     
                      404, 500, etc.)   minor errors in   with incomplete                   events or                        
                      with accurate     details.          or incorrect                      provides                         
                      event details.                      details.                          incorrect                        
                                                                                            details.                         

  **Troubleshooting   Proposes logical, Solutions are     Solutions are                     Solutions are                    /10
  Solutions**         effective         mostly correct    somewhat vague                    unclear or                       
                      solutions to all  but miss some key or incomplete.                    incorrect.                       
                      identified        points.                                                                              
                      issues.                                                                                                

  **Report Structure  Well-organized    Report is mostly  Report is                         Report is                        /10
  & Clarity**         report with all   organized with    disorganized or                   unclear or                       
                      sections clearly  minor formatting  missing                           incomplete.                      
                      completed.        issues.           sections.                                                          

  **Recommendations   Provides          Recommendations                   Recommendations                 Fails to provide   /10
  for Monitoring**    thoughtful,       are relevant but                  are vague or                    relevant           
                      proactive         lack depth.                       incomplete.                     recommendations.   
                      recommendations                                                                                        
                      to prevent future                                                                                      
                      issues.                                                                                                

  **Participation &   Actively engaged  Participated but                  Minimal                         Did not            /10
  Effort**            in the activity,  required some                     participation,                  participate        
                      followed          guidance.                         needed                          meaningfully.      
                      instructions                                        significant help.                                  
                      thoroughly.                                                                                            

  **Score**                                                                                                                  **/50**
  ---------------------------------------------------------------------------------------------------------------------------------------
