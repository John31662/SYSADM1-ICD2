+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| ddfd7a934a2c445cb2cf1547396c5930 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME:                            | DATE PERFORMED:        | /50      |
+----------------------------------+------------------------+----------+
| Section:                         | DATE SUBMITTED:        |          |
+----------------------------------+------------------------+----------+

1.  # SYSADM1 -- Setting Up Webserver

    # Requirement: 

-   A virtual machine running Linux and Windows OS

> Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

3.  Configure the Website:

    -   Right-click on your website and select Edit.

    -   Set the Default Document to the name of your main HTML file
        \>default.html

    -   Configure other settings as needed (e.g., SSL certificates,
        authentication)

4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

> ![](vertopal_ddfd7a934a2c445cb2cf1547396c5930/media/image2.png){width="3.652083333333333in"
> height="1.52377624671916in"}

-   Save it as default.html or your preferred name.

5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

> Grading Rubric

  ----------------- ------------ -----------------------------------------------
  **Criteria**      **Points**   **Description**

  Web Server        15           Correctly installs IIS or another web server on
  Installation                   the virtual machine.

  Website           15           Successfully configures the website with the
  Configuration                  correct physical path, IP address, port, and
                                 default document.

  Successful Access 15           Successfully accesses the web page from the
                                 client computer using the correct URL.

  Troubleshooting   15           Demonstrates ability to troubleshoot common
                                 issues, such as network connectivity problems
                                 or configuration errors.

  Documentation     10           Provides clear and concise documentation of the
                                 installation, configuration, and testing
                                 process.

  Total             /70          
  ----------------- ------------ -----------------------------------------------

> **Screenshots:**
>
> **ISS installed**
>
> ![](vertopal_ddfd7a934a2c445cb2cf1547396c5930/media/image3.png){width="5.95459208223972in"
> height="4.845939413823272in"}
>
> **Website creation**
>
> ![](vertopal_ddfd7a934a2c445cb2cf1547396c5930/media/image4.png){width="3.3546347331583553in"
> height="0.8334492563429571in"}
>
> **Web page file (on server)**
>
> ![](vertopal_ddfd7a934a2c445cb2cf1547396c5930/media/image5.png){width="7.027083333333334in"
> height="1.1729166666666666in"}
>
> **Default document**
>
> ![](vertopal_ddfd7a934a2c445cb2cf1547396c5930/media/image6.png){width="3.5629975940507435in"
> height="4.156829615048119in"}
>
> **Web server testing**
>
> ![](vertopal_ddfd7a934a2c445cb2cf1547396c5930/media/image7.png){width="5.269660979877515in"
> height="3.9932556867891513in"}
>
> ![](vertopal_ddfd7a934a2c445cb2cf1547396c5930/media/image8.png){width="6.782195975503062in"
> height="3.135854111986002in"}
