<style>
    /* Set fill and line colors for certification boxes. dk suffix means "dark" for the line color. */
    :root {
            --green: #70AD47;
            --greendk: #548235;
            --teal: #008080;
            --tealdk: #003F3E;
            --orange: #fa8e36;
            --orangedk: #c06216;
            --orangelt: #fdeada;
            --yellow: #e4ac03;
            --yellowdk: #7F6000;
            --black: #2a2a2a;
            --blackdk: #000000; 
            --blacklt: #d9d9d9;
            --purple: #683e9b;
            --purpledk: #352647;
            --purplelt: #eddbff;
            --skyblue: #6bb3f6;
            --skybluedk: #2665a0;
            --blue: #2e5688;
            --bluedk: #1f3147;
            --bluelt: #dce6f2;
            --red: #c0514d;
            --reddk: #8c3736;
            --redlt: #f2dcdb;
            --magenta: #830083;
            --magentadk: #490e49;
    }

    /* I think this is vestigial April 2022
    .cert-body {
           margin-left: 6vmax;
            margin-right: 6vmax;
    }
    .cert-list {
            margin-left: 8vmax;
            margin-right: 6vmax;
    }
    */

    /* Style for the text at the bottom right of the chart */
    .key {
            color: #000000;
            padding: 0.2vmax;
            font-size: 1vmax;
            text-align: right;
            display: grid;
            grid-template-rows: 1.68vmax;
            grid-column-gap: 0.2vmax;
            grid-gap: 0.1vmax;
    }

    /* Primary style for the chart, which is the parent container for everything else. */
    .certchart {
            background: white;
            color: #323232;
            font-weight: 300;
            margin-top: 1vmax;
            margin-left: 1vmax;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            font-family: "Segoe UI", "Calibri", Tahoma, "Geneva", Verdana, sans-serif;
            float: left;
    }
    
    /* Background grid for domain titles and borders */
    .certbg {
            background: #ffffff;
            justify-content: left;
            display: grid;
            position: relative;
            grid-template-columns: [silllevel] 0.8vmax [network] 7.5vmax [iam] 2.65vmax [engineer] 17.2vmax [asset] 5.1vmax [mgmt] 21.8vmax [testing] 7.5vmax [software] 2.7vmax [operations] 31.5vmax;
            grid-template-rows: [domain] 2vmax [chart] 43.7vmax;
            column-gap: 0.2vmax;
            /* row-gap: 0.2vmax; */
            white-space: pre-wrap;
            line-height: 130%;
            left: -0.7vmax;
    }
    
    /* Style for the title text of each domain */
    .domaintitle {
            font-weight: 450;
            font-size: 0.8vmax;
            text-align: center;
            align-content: bottom;
            justify-content: center;
            align-self: flex-end;
            display: flex;
            margin-bottom: 0.1vmax;
    }
    
    /* Styles for each certification domain box. This also allows for the placement of sub-domain shaded boxes. */
    .skilllevelcontainer {
            display: grid;
    }

    .networkcontainer {
            display: grid;
            border: 2px solid var(--green);
            border-radius: 0.25vmax;
    }
    
    .iamcontainer {
            display: grid;
            border: 2px solid var(--teal);
            border-radius: 0.25vmax;
    }
    
    .engineercontainer {
            display: grid;
            border: 2px solid var(--orange);
            border-radius: 0.25vmax;
            grid-template-columns: 2.3vmax 2.3vmax 2.2vmax 2.2vmax 2.2vmax 2.2vmax 2.2vmax;
            grid-template-rows: 1vmax auto;
            column-gap: 0.2vmax;
    }
    
    .assetcontainer {
            display: grid;
            border: 2px solid var(--yellow);
            border-radius: 0.25vmax;
    }
    
    .mgmtcontainer {
            display: grid;
            border: 2px solid var(--black);
            border-radius: 0.25vmax;
            grid-template-columns: 2.2vmax 2.2vmax 2.2vmax 2.2vmax 2.3vmax 2.2vmax 2.2vmax 2.2vmax 2.2vmax;
            grid-template-rows: 1vmax auto;
            column-gap: 0.2vmax;
    }
    
    .testingcontainer {
            display: grid;
            border: 2px solid var(--magenta);
            border-radius: 0.25vmax;
    }
    
    .softwarecontainer {
            display: grid;
            border: 2px solid var(--skyblue);
            border-radius: 0.25vmax;
    }
    
    .operationscontainer {
            display: grid;
            border: 2px solid var(--red);
            border-radius: 0.25vmax;
            grid-template-columns: 2.2vmax 2.2vmax 2.2vmax 2.3vmax 2.2vmax 2.3vmax 2.2vmax 2.2vmax 2.2vmax 2.2vmax 2.2vmax 2.2vmax 2.1vmax;
            grid-template-rows: 1vmax auto;
            column-gap: 0.2vmax;
    }
    
    /* Style for sub-domain titles. Mostly to allow for proper spanning. */
    .subtitle1 {
            font-weight: 400;
            font-size: 0.5vmax;
            text-align: center;
            align-content: bottom;
            justify-content: center;
            align-self: flex-end;
            display: flex;
    }
    
    .subtitle2 {
            font-weight: 400;
            font-size: 0.5vmax;
            text-align: center;
            align-content: bottom;
            justify-content: center;
            align-self: flex-end;
            display: flex;
            grid-column: span 2;
    }
    
    .subtitle3 {
            font-weight: 400;
            font-size: 0.5vmax;
            text-align: center;
            align-content: bottom;
            justify-content: center;
            align-self: flex-end;
            display: flex;
            grid-column: span 3;
    }

    .subtitle4 {
            font-weight: 400;
            font-size: 0.5vmax;
            text-align: center;
            align-content: bottom;
            justify-content: center;
            align-self: flex-end;
            display: flex;
            grid-column: span 4;
    } 
    .subtitle5 {
            font-weight: 400;
            font-size: 0.5vmax;
            text-align: center;
            align-content: bottom;
            justify-content: center;
            align-self: flex-end;
            display: flex;
            grid-column: span 5;
    }
    
    /* Style for certification boxes, separated by domain for proper coloring. Also used to indicate how many boxes to span the certs. */
    .engsubdomain1 {
            display: flex;
            background: var(--orangelt);
            column-gap: 1vmax;
    }
    
    .engsubdomain4 {
            display: flex;
            background: var(--orangelt);
            grid-column: span 4;
            column-gap: 1vmax;
            margin-left: 0.3vmax;
    }
    
    .mgmtsubdomain4 {
            display: flex;
            background: var(--blacklt);
            grid-column: span 4;
            column-gap: 1vmax;
			margin-left: 0.3vmax;
    }
    
    .bluesubdomain2 {
            display: flex;
            background: var(--bluelt);
            grid-column: span 2;
            margin-left: 0.1vmax;
    }
    
    .redsubdomain2 {
            display: flex;
            background: var(--redlt);
            grid-column: span 2;
            column-gap: 1vmax;
    }
    
    .redsubdomain5 {
            display: flex;
            background: var(--redlt);
            grid-column: span 5;
            column-gap: 1vmax;
    }

    /* Foreground grid for certification squares */
    .certcontainer {
            justify-content: center;
            text-align: center;
            align-content: center;
            line-height: 120%;
            display: grid;
            position: absolute;
            font-size:0.6vmax;
            top: 4.8vmax;
            left: -0.31vmax;
            grid-template-columns: [skilllevel] 1.7vmax [network] 2.3vmax 2.3vmax 2.3vmax .4vmax [iam] 2.3vmax .4vmax [engineer] 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 0.4vmax [asset] 2.3vmax 2.3vmax 0.4vmax [mgmt] 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 0.4vmax [testing] 2.3vmax 2.3vmax 2.3vmax 0.4vmax [software] 2.3vmax 0.4vmax [ops] 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax 2.3vmax;
            grid-template-rows: repeat(27, 1.5vmax);
            column-gap: 0.1vmax;
            row-gap: 0.1vmax;
            white-space: pre-wrap;
    }
    
    /* Skill level grid overlayed on top of .certcontainer to show
    .skilllevel {
        justify-content: center;
        text-align: center;
        align-content: center;
        line-height: 120%;
        display: grid;
        position: absolute;
        font-size:0.6vmax;
        top: 3.5vmax;
        left: 2.6vmax;
        grid-template-columns: max-content;
        grid-template-rows: 13.5vmax 22.5vmax 7.5vmax;
        column-gap: 0.1vmax;
        row-gap: 0.1vmax;
        white-space: pre-wrap;        
    } */

    .spacer {
            background: none;
    }
    
    .spacer5 {
            background: none;
            grid-column: span 5;
    }
    
    .spacer10 {
            background: none;
            grid-column: span 10;
    }
    
    .skilllevelitem {
            transform: rotate(270deg);
            justify-items: right;
            align-items: flex-end;
            font-weight: 600;
            font-size: 0.8vmax;
            display: grid;
    }

    .networkitem1 {
            background: var(--green);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--greendk);
            border-radius: 0.25vmax;
    }
    
    .networkitem2 {
            background: var(--green);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--greendk);
            border-radius: 0.25vmax;
            grid-column: span 3;
    }
    
    .iamitem1 {
            background: var(--teal);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--tealdk);
            border-radius: 0.25vmax;
    }
    
    .engineeritem1 {
            background: var(--orange);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--orangedk);
            border-radius: 0.25vmax;
    }
    
    .engineeritem2 {
            background: var(--orange);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--orangedk);
            border-radius: 0.25vmax;
            grid-column: span 3;
    }
    
    .engineeritem3 {
            background: var(--orange);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--orangedk);
            border-radius: 0.25vmax;
            grid-column: span 5;
    }
    
    .engineeritem4 {
            background: var(--orange);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--orangedk);
            border-radius: 0.25vmax;
            grid-column: span 6;
    }
    
    .assetitem1 {
            background: var(--yellow);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--yellowdk);
            border-radius: 0.25vmax;
    }
    
    .assetitem2 {
            background: var(--yellow);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--yellowdk);
            border-radius: 0.25vmax;
            grid-column: span 3;
    }
    
    .mgmtitem1 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
    }
    
    .mgmtitem2 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 3;
    }

    .mgmtitem4x {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 4;
    }

    .mgmtitem3 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 5;
    }
    
    .mgmtitem4 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 6;
    }
    
    .mgmtitem5 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 6;
    }
    
    .mgmtitem15 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 19;
    }
    
    .mgmtitem17 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 22;
    }
    .mgmtitemCASP {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 22;
    }   
    .mgmtitem25 {
            background: var(--black);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--blackdk);
            border-radius: 0.25vmax;
            grid-column: span 32;
    }
    
    .testitem1 {
            background: var(--purple);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--purpledk);
            border-radius: 0.25vmax;
    }
    
    .testitem2 {
            background: var(--purple);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--purpledk);
            border-radius: 0.25vmax;
            grid-column: span 3;
    }
    
    .softwareitem1 {
            background: var(--skyblue);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--skybluedk);
            border-radius: 0.25vmax;
    }
    
    .softwareitem2 {
            background: var(--skyblue);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--skybluedk);
            border-radius: 0.25vmax;
            grid-column: span 3;
    }
    
    .softwareitem6 {
            background: var(--skyblue);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--skybluedk);
            border-radius: 0.25vmax;
            grid-column: span 9;
    }
    
    .blueopsitem1 {
            background: var(--blue);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--bluedk);
            border-radius: 0.25vmax;
    }
    
    .blueopsitem2 {
            background: var(--blue);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--bluedk);
            border-radius: 0.25vmax;
            grid-column: span 2;
    }
    
    .blueopsitem3 {
            background: var(--blue);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--bluedk);
            border-radius: 0.25vmax;
            grid-column: span 5;
    }

    .blueopsitem9 {
            background: var(--blue);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--bluedk);
            border-radius: 0.25vmax;
            grid-column: span 11;
    }
    
    .redopsitem1 {
            background: var(--red);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--reddk);
            border-radius: 0.25vmax;
    }
    
    .redopsitem2 {
            background: var(--red);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--reddk);
            border-radius: 0.25vmax;
            grid-column: span 2;
    }
    
    .redopsitem3 {
            background: var(--red);
            color: #ffffff;
            font-weight: 400;
            align-items: center;
            justify-items: center;
            text-decoration: none;
            display: grid;
            border: 0.05vmax solid var(--reddk);
            border-radius: 0.25vmax;
            grid-column: span 3;
    }

    /* Draft of different tooltip
    .tooltiptext {
        visibility: hidden;
        background: inherit;
        color: inherit;
        text-align: left;
        padding: 0.3vmax;
        border-radius: 0.2vmax;
        
        position:absolute;
        bottom: 97%;
        left: 50%;
        margin-left: -17.8%;
    }
    
    .mgmtitem25:hover .tooltiptext {
        visibility: visible;
    }

    .tooltiptext::after {
        content: " ";
        position: absolute;
        top: 100%;
        left: 50%;
        margin-left: -5px;
        border-width: 5px;
        border-style: solid;
        border-color: black transparent transparent transparent;
    } */
    
    /* Certification tooltip hover text format */
    [tooltiptext]:before {
        position: absolute;
        content: attr(tooltiptext);
        width: max-content;
        height: max-content;
        padding: 0.4vmax;
        background: inherit;
        border: inherit;
        border-radius: 0.2vmax;
        color: inherit;
        text-align: left;
        display: none;
        font-size: 125%;
    }
    
    [tooltiptext]:hover:before {
        display: block;    
    }
    
    [tooltiptexttitle]:before {
        position: absolute;
        content: attr(tooltiptexttitle);
        width: 25vmax;
        height: max-content;
        padding: 0.4vmax;
        background: var(--black);
        border: var(--blackdk);
        border-radius: 0.2vmax;
        color: white;
        text-align: left;
        display: none;
        font-size: 100%;
        z-index: 1;

        top: 4.5%;
    }
    
    [tooltiptexttitle]:hover:before {
        display: block;    
    }
    
    [tooltiptexttitleleft]:before {
        position: absolute;
        content: attr(tooltiptexttitleleft);
        width: 25vmax;
        height: max-content;
        padding: 0.4vmax;
        background: var(--black);
        border: var(--blackdk);
        border-radius: 0.2vmax;
        color: white;
        text-align: left;
        display: none;
        font-size: 100%;
        z-index: 1;

        top: 4.5%;
        left: 0%;
    }

    [tooltiptexttitleleft]:hover:before {
        display: block;    
    }

    [tooltipleft]:before {
        position: absolute;
        content: attr(tooltipleft);
        width: max-content;
        height: max-content;
        padding: 0.4vmax;
        background: inherit;
        border: inherit;
        border-radius: 0.2vmax;
        color: inherit;
        text-align: left;
        display: none;
        font-size: 125%;
        line-height: 125%;

        left: 1%;
    }

    [tooltipleft]:hover:before {
        display: block;    
    }

    [tooltipright]:before {
        position: absolute;
        content: attr(tooltipright);
        width: max-content;
        height: max-content;
        padding: 0.4vmax;
        background: inherit;
        border: inherit;
        border-radius: 0.2vmax;
        color: inherit;
        text-align: left;
        display: none;
        font-size: 125%;
        line-height: 125%;

        right: 0%;
    }

    [tooltipright]:hover:before {
        display: block;    
    }

    /* Make a static image if horizontal screen is smaller than 898px (iPhone size is 898)*/
    #interactive {display: block;}
    #static {display: none;}
    
    @media screen and (max-width: 897px) {
    
      #interactive {display: none;}
      #static {display: block;}
    
    }
    </style>
    
    <div id="static">
            <img src="https://pauljerimy.com/wp-content/uploads/2022/03/SCRApril2022.png" alt="Static Security Certification Chart (April 2022)" class="wp-image-309">
    </div>
    
    <div id="interactive" class="certchart">
        <div style="text-align:left;font-size:200%;font-weight:500;padding-bottom:0.2vmax;">Security Certification Roadmap

        </div>
        <!-- Begin Background Grid -->
            <div class="certbg"> <!-- Domain Title Row-->
                    <div class="domaintitle"></div>
                    <div class="domaintitle" style="color:var(--green);" tooltiptexttitleleft="     The communication and network security domain covers the ability to secure communication channels and networks. Topics include secure and converged protocols, wireless networks, cellular networks, hardware operation (warranty and redundant power) and third-party connectivity.  IP networking (IPSec, IPv4 and IPv6) are also included in this domain.">Communication and Network Security</div>
                    <div class="domaintitle" style="color:var(--teal);" tooltiptexttitleleft="     The identity and access management domain covers the attacks that target the human gateway to gain access to data. Other topics include ways to identify users with rights to access the information and servers. Identify and access management covers the topics of applications, Single sign-on authentication, privilege escalation, Kerberos, rule-based or risk-based access control, proofing and establishment of identity.">IAM</div>
                    <div class="domaintitle" style="color:var(--orange);" tooltiptexttitle="     The security architecture and engineering domain covers important topics concering security engineering plans, designs, and principles. Topics include assessing and mitigating information system vulnerabilities, fundamental concepts of security models and security architectures in critical areas like access control. Cloud systems, cryptography, system infiltrations (ransomware, fault-injection and more) and virtualized systems are also covered in this domain.">Security Architecture and Engineering</div>
                    <div class="domaintitle" style="color:var(--yellow);" tooltiptexttitle="     The Asset Security domain deals with the issues related to the collection, storage, maintenance, retention and destruction of data. It also covers knowledge of different roles regarding data handling (owner, controller and custodian) as well as data protection methods and data states. Other topics include resource provision, asset classification and data lifecycle management.">Asset Security</div>
                    <div class="domaintitle" style="color:var(--black);" tooltiptexttitle="     The security and risk management domain covers general on skills related to the implementation of user awareness programs as well as security procedures. Emphasis is also placed on risk management concerning the acquisition of new services, hardware and software (supply chain). Other skills include social engineering defense mechanisms.">Security and Risk Management</div>
                    <div class="domaintitle" style="color:var(--purple);" tooltiptexttitle="     The security assessment and testing domain deals with all the techniques and tools used to find system vulnerabilities, weaknesses and potential areas of concern not addressed by security procedures and policies. Attack simulations, vulnerability assessment, compliance checks, and ethical disclosure also fall under this domain.">Security Assessment and Testing</div>
                    <div class="domaintitle" style="color:var(--skyblue);" tooltiptexttitle="     The software development security domain deals with implementing software-based security protocols within environments for which the IT professional is responsible. Risk analysis, vulnerability identification and auditing of source codes are all covered in this subset. Additional topics include software-designed security, maturity models, development methodologies, open-source and third-party development security.">Software Security</div>
                    <div class="domaintitle" style="color:var(--red);" tooltiptexttitle="     The security operations domain covers topics ranging from investigations and digital forensic to detection and intrusion prevention tools, sandboxing and firewalls. Topics include user and entity behavior analytics, threat intelligence (threat hunting and threat feeds) log management, artifacts (mobile, computer and network), machine learning and AI-based tools, penetration testing, and exploitation development.">Security Operations</div>
                    <div class="skilllevel"></div>
                    <div class="networkcontainer"></div>
                    <div class="iamcontainer"></div>
                    <div class="engineercontainer">
                            <div class="subtitle4">Cloud/SysOps</div>
                            <div class="subtitle1">*nix</div>
                            <div class="subtitle1">ICS/IoT</div>
                            <div class="spacer"></div>
                            <div class="engsubdomain4"></div>
                            <div class="engsubdomain1"></div>
                            <div class="engsubdomain1"></div>
                            <div class="spacer"></div>
                    </div>
                    <div class="assetcontainer"></div>
                    <div class="mgmtcontainer">
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="subtitle4">GRC</div>
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="mgmtsubdomain4"></div>
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                    </div>
                    <div class="testingcontainer"></div>
                    <div class="softwarecontainer"></div>
                    <div class="operationscontainer">
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="subtitle2">Forensics</div>
                            <div class="subtitle2">Incident Handling</div>
                            <div class="subtitle5">Penetration Testing</div>
                            <div class="subtitle2">Exploitation</div>
                            <div class="spacer"></div>
                            <div class="spacer"></div>
                            <div class="bluesubdomain2"></div>
                            <div class="bluesubdomain2"></div>
                            <div class="redsubdomain5"></div>
                            <div class="redsubdomain2"></div>
                    </div>                
            </div>
            <!-- Begin Foreground Grid -->
            <div class="certcontainer">
                    <!-- Row 1 (intentionally blank to make room for sub-domain titles)-->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer10"></div>
                    <div class="spacer10"></div>
                    <div class="spacer10"></div>
                    <div class="spacer10"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 2 -->
                    <div class="spacer"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer10"></div>
                    <a class="redopsitem1" href="https://www.offensive-security.com/awe-osee/" tooltipright="Offensive Security Exploitation Expert
    $5,000 lab
    Plus travel" tabindex="0" target="_blank" >OSEE</a>
                    <div class="spacer"></div>
                    <!-- Row 3 -->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="networkitem2" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/expert/ccie-security.html" tooltiptext="Cisco Certified Implementation Expert - Security
    $2,050 Hands-on Lab
    $12,000 est Travel cost" tabindex="0" target="_blank" >CCIE Sec</a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.crest-approved.org/examination/technical-security-architecture/index.html" tooltiptext="CREST Registered Technical Security Architect
    $2,300 two exams
    In person in the UK" tabindex="0" target="_blank" >CREST CRTSA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem2" href="https://www.axelos.com/certifications/itil-certifications/itil-master" tooltiptext="ITIL Master
    $4,000 Interview" tabindex="0" target="_blank" >ITIL Master</a>
                    <div class="spacer10"></div>
                    <div class="spacer10"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://help.offensive-security.com/hc/en-us/articles/4403282452628-What-is-OSCE3-" tooltiptext="Offensive Security Certified Expert 3
    $4,649 3 labs" tabindex="0" target="_blank" >OSCE3</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 4 -->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="networkitem2" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/expert/ccie-security-v2.html" tooltipleft="Cisco Certified Internetwork Expert - Enterprise Infrastructure
    ~$2,050 hands-on lab
    ~$12,000 in travel costs" tabindex="0" target="_blank" >CCIE Ent</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.vmware.com/education-services/certification/vcdx-dcv.html" tooltiptext="VMware Certified Design Expert in Datacenter Virtualization
    $3,995 exams
    Application also req." tabindex="0" target="_blank" >VCDX DCV</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.redhat.com/en/services/certification/rhca" tooltiptext="Red Hat Certified Architect
    ~$3,745 exam
    plus travel" tabindex="0" target="_blank" >RHCA</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://sabsa.org/certification/" tooltiptext="SABSA Chartered Security Architect - Master Certificate
    $3,750 exam &amp; thesis
    Branded course required" tabindex="0" target="_blank" >SABSA SCM</a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem4x" href="https://www.giac.org/get-certified/giac-portfolio-certifications/#GSE" tooltiptext="GIAC Security Expert
    ~$7475 for 10 exams" tabindex="0" target="_blank" ><b>GSE</b></a>
                    <div class="spacer5"></div>
                    <a class="blueopsitem3" href="https://www.giac.org/certifications/reverse-engineering-malware-grem/" tooltiptext="GIAC Reverse Engineering Malware
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GREM</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.offensive-security.com/awae-oswe/" tooltiptext="Offensive Security Web Expert
    ~$1649 lab" tabindex="0" target="_blank" >OSWE</a>
                    <div class="spacer"></div>
                    <a class="redopsitem2" href="https://www.offensive-security.com/pen300-osep/" tooltipright="Offensive Security Experienced Penetration Tester
    $1,499 lab" tabindex="0" target="_blank" >OSEP</a>
                    <a class="redopsitem1" href="https://www.offensive-security.com/exp301-osed/" tooltipright="Offensive Security Exploit Developer
    $1,499 lab" tabindex="0" target="_blank" >OSED</a>
                    <!-- Row 5 -->
                    <div class="spacer"></div>
                    <div class="spacer10"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.pmi.org/certifications/types/program-management-pgmp" tooltiptext="PMI Program Management Professional
    $1,000 exam" tabindex="0" target="_blank" >PgMP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem4x" href="https://www.isc2.org/certifications#Specialized" tooltiptext="(ISC)2 Certified Information Systems Security Professional Concentrations
    $599 exam" tabindex="0" target="_blank" ><b>CISSP Concentrations</b></a>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.ncsc.gov.uk/information/about-certified-professional-scheme" tooltiptext="NCSC Certified Cybersecurity Professional - Lead Practitioner
    $1388 interview" tabindex="0" target="_blank" >NCSC CCPLP</a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.iacis.com/certification/" tooltiptext="IACIS Certified Forensic Computer Examiner
    $750 4 peer reviewed exams" tabindex="0" target="_blank" >CFCE</a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem2" href="https://www.giac.org/certification/gxpn" tooltipright="GIAC Exploit Researcher and Advanced Penetration Tester
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GXPN</a>
                    <div class="spacer"></div>
                    <!-- Row 6 -->
                    <div class="skilllevelitem"><span style="color:var(--reddk)">Expert</span></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.vmware.com/education-services/certification/vcap-dcv-design.html" tooltiptext="VMware Certified Implementation Expert in Datacenter Virtualization
    $900 two exams" tabindex="0" target="_blank" >VCIX DCV</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="assetitem2" href="https://www.asisonline.org/certification/certified-protection-professional-cpp/" tooltiptext="ASIS Certified Protection Professional
    $485 exam" tabindex="0" target="_blank" >ASIS CPP</a>
                    <a class="mgmtitem1" href="https://www.zachman.com/certification/what-we-certify/enterprise-architect" tooltiptext="Zachman Enterprise Architect Professional (Level 3)
    $2,999 exam &amp; case study
    Level 1 &amp; 2 cert not req'd" tabindex="0" target="_blank" >Zach EAPro</a>
                    <a class="mgmtitem1" href="https://www.pmi.org/certifications/project-management-pmp" tooltiptext="PMI Project Management Professional
    $555 exam" tabindex="0" target="_blank" >PMP</a>
                    <a class="mgmtitem1" href="https://www.isaca.org/credentialing/cism" tooltiptext="ISACA Certified Information Security Manager
    $760 exam" tabindex="0" target="_blank" >CISM</a>
                    <a class="mgmtitem1" href="https://www.seco-institute.org/certifications/information-security-certification-track/" tooltiptext="SECO Information Security Management Expert
    $850 exam" tabindex="0" target="_blank" >S-ISME</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.ncsc.gov.uk/information/about-certified-professional-scheme" tooltiptext="NCSC Certified Cybersecurity Professional - Senior Practitioner
    $907 interview" tabindex="0" target="_blank" >NCSC CCPSP</a>
                    <div class="spacer5"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.csiac.org/certification/cybersecurity-forensic-analyst-csfa-certification/" tooltiptext="CSIAC CyberSecurity Forensic Analyst
    $750 exam &amp; lab" tabindex="0" target="_blank" >CSFA</a>
                    <a class="blueopsitem2" href="https://www.giac.org/certifications/ios-macos-examiner-gime/" tooltiptext="GIAC iOS and MacOS Examiner
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GIME</a>
                    <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
                    <a class="redopsitem2" href="https://www.giac.org/certification/gawn" tooltipright="GIAC Assessing Wireless Networks
    $979 exam
    SANS course recommended" tabindex="0" target="_blank">GAWN</a>
                    <div class="spacer"></div>
                    <!-- Row 7 -->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem4x" href="https://www.isc2.org/Certifications/CISSP" tooltiptext="(ISC)2 Certified Information Systems Security Professional
    $749 exam" tabindex="0" target="_blank" ><b>CISSP</b></a>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <a class="blueopsitem1" href="https://cyberdefenders.org/blue-team-training/courses/certified-cyberdefender-certification/" tooltiptext="Certified CyberDefender
    $800 course
    2 exam attempt included" tabindex="0" target="_blank">CCD</a>
                    <a class="blueopsitem1" href="https://www.iacis.com/certification/cawfe/" tooltiptext="IACIS Certified Advanced Windows Forensic Examiner
    $750 written exam &amp; lab" tabindex="0" target="_blank" >CAWFE</a>
                    <a class="blueopsitem2" href="https://www.giac.org/certification/gcfa" tooltiptext="GIAC Certified Forensic Analyst
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCFA</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certification/gcti" tooltiptext="GIAC Cyber Threat Intelligence
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCTI</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem2" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-simulated-attack-manager" tooltipright="CREST Certified Simulated Attack Manager
    $2,499 2 exams" tabindex="0" target="_blank" >CREST CSAM</a>
                    <div class="spacer"></div>
                    <!-- Row 8 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.juniper.net/us/en/training/certification/certification-tracks/junos-security-track/?tab=jnciesec" tooltipleft="Juniper Networks Certified Internet Expert, Security
    $1,400 Hands-on Lab" tabindex="0" target="_blank" >JNCIE Sec</a>
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/expert/ccde.html" tooltiptext="Cisco Certified Design Expert
    ~$1,600 written exam
    with hands-on lab" tabindex="0" target="_blank" >CCDE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://aws.amazon.com/certification/certified-solutions-architect-professional/" tooltiptext="Amazon Web Services Certified Solutions Architect - Professional
    $300 exam" tabindex="0" target="_blank" >AWS SAP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.redhat.com/en/services/certification/rhce" tooltiptext="Red Hat Certified Engineer
    $400 exam" tabindex="0" target="_blank" >RHCE</a>
                    <a class="engineeritem1" href="https://www.giac.org/certification/defending-advanced-threats-gdat" tooltiptext="GIAC Defending Advanced Threats
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GDAT</a>
                    <a class="engineeritem1" href="https://docs.microsoft.com/en-us/certifications/exams/sc-100" tooltiptext="Microsoft Cybersecurity Architect
    $165 exam" tabindex="0" target="_blank" >SC-100</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem2" href="https://www.opengroup.org/certifications/togaf" tooltiptext="OpenGroup TOGAF Certified
    $360 exam" tabindex="0" target="_blank" >TOGAF</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://ciso.eccouncil.org/cciso-certification/" tooltiptext="EC Council Certified Information Security Officer
    $3,150 course exam
    Branded course required" tabindex="0" target="_blank" >CCISO</a>
                    <a class="mgmtitem1" href="https://www.exin.com/certifications/information-security-management-expert-based-isoiec-27001-exam" tooltiptext="EXIN Information Security Management Expert
    EST $799 oral exam" tabindex="0" target="_blank" >EEXIN ISM</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.giac.org/certification/gstrt" tooltiptext="GIAC Strategic Planning, Policy and Leadership
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GSTRT</a>
                    <a class="mgmtitem1" href="https://www.ncsc.gov.uk/information/about-certified-professional-scheme" tooltiptext="NCSC Certified Cybersecurity Professional - Practitioner
    $225 interview" tabindex="0" target="_blank" >NCSC CCPP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="testitem1" href="https://www.giac.org/certification/gsna" tooltiptext="GIAC Systems and Network Auditor
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GSNA</a>
                    <div class="spacer5"></div>
                     <a class="blueopsitem1" href="https://www.opentext.com/products-and-solutions/services/training-and-learning-services/encase-training/forensic-security-responder-certification" tooltiptext="OpenText Certified Forensic Security Responder
    $250 written exam &amp; lab" tabindex="0" target="_blank" >CFSR</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certification/network-forensic-analyst-gnfa" tooltiptext="GIAC Network Forensic Analyst
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GNFA</a>
                    <div class="spacer"></div>
		    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://elearnsecurity.com/product/ewptxv2-certification/" tooltiptext="eLearnSecurity Web Application Penetration Tester eXtreme
    $400 exam
    $2000 training" tabindex="0" target="_blank" >eWPTX</a>
                    <a class="redopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-simulated-attack-specialist" tooltiptext="CREST Certified Simulated Attack Specialist
    $2,520 2 exams &amp; lab" tabindex="0" target="_blank" >CREST CCSAS</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 9 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcx_cybersecurity" tooltipleft="Fortinet Certified Expert
                    $400 written exam
                    $1600 in-person lab" tabindex="0" target="_blank" >FCX</a>
                    <div class="spacer5"></div>
                    <a class="engineeritem1" href="https://docs.microsoft.com/en-us/learn/certifications/azure-solutions-architect?wt.mc_id=learningredirect_certs-web-wwl" tooltiptext="Microsoft Azure Solutions Architect Expert
    $330 exam" tabindex="0" target="_blank" >AZ-305</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.vmware.com/education-services/certification/vcap-nv-deploy.html" tooltiptext="VMware Certified Implementation Expert in Network Virtualization
    $900 two exams" tabindex="0" target="_blank" >VCIX NV</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.lpi.org/our-certifications/lpic-3-303-overview" tooltiptext="Linux Professional Institute Certified: 303 Security
    $200 exam" tabindex="0" target="_blank" >LPIC-3</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://sabsa.org/certification/" tooltiptext="SABSA Chartered Security Architect - Practitioner Certificate
    $3,750 written exam
    Branded course required" tabindex="0" target="_blank" >SABSA SCP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.scrum.org/assessments/professional-scrum-master-iii-certification" tooltiptext="Scrum.org Professional Scrum Master III
    $500 exam
    Branded course required" tabindex="0" target="_blank" >PSM III</a>
                    <a class="mgmtitem4x" href="https://www.giac.org/get-certified/giac-portfolio-certifications/#gsp" tooltiptext="GIAC Security Professional
    ~$3735 for 5 exams" tabindex="0" target="_blank" ><b>GSP</b></a>
                    <a class="mgmtitem1" href="https://www.giac.org/certification/gisp" tooltiptext="GIAC Information Security Professional
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GISP</a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mtia-certified-threat-intelligence-analyst.html" tooltiptext="Mosse Institute Certified Threat Intelligence Analyst Certification
  $450 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MTIA</a>
		    <a class="blueopsitem1" href="https://www.giac.org/certifications/cloud-forensics-responder-gcfr/" tooltiptext="GIAC Cloud Forensics Responder
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCFR</a>
                    <a class="blueopsitem2" href="https://securityblue.team/btl2/" tooltiptext="Security Blue Team Level 2
    $2,190 course
    1 exam attempt included" tabindex="0" target="_blank">BTL2</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.mosse-institute.com/certifications/mrt-certified-red-teamer.html" tooltiptext="Mosse Institute Certified Red Teamer Certification
  $450 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MRT</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="hhttps://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-infrastructure-tester" tooltiptext="CREST Certified Infrastructure Tester
    $2,520 exam &amp; lab" tabindex="0" target="_blank" >CREST CCTINF</a>
                    <a class="redopsitem1" href="https://academy.hackthebox.com/preview/certifications/htb-certified-web-exploitation-expert" tooltiptext="Hack the Box Certified Web Exploitation Expert
    $1260 Subscription available" tabindex="0" target="_blank" >HTB CWEE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 10 -->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://cloud.google.com/certification/cloud-architect" tooltiptext="Google Professional Cloud Architect
    $200 exam" tabindex="0" target="_blank" >Google PCSA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.suse.com/training/exam/sce-sles-15/" tooltiptext="SUSE Certified Engineer
    $195 practical exam" tabindex="0" target="_blank" >SCE</a>
                    <a class="engineeritem1" href="https://www.isa.org/training-and-certifications/isa-certification/isa99iec-62443/isa99iec-62443-cybersecurity-certificate-programs/" tooltiptext="ISA Cybersecurity Expert
    $2,700 course + exam
    Course required" tabindex="0" target="_blank" >ISA CE</a>
                    <a class="engineeritem1" href="https://www.giac.org/certification/defensible-security-architecture-gdsa" tooltiptext="GIAC Defensible Security Architecture
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GDSA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.axelos.com/certifications/itil-certifications/itil-strategic-leader-itil-4" tooltiptext="ITIL Strategic Leader
    $4,800 two course exams
    2 branded courses required" tabindex="0" target="_blank" >ITIL SL</a>
                    <a class="mgmtitem1" href="https://www.zachman.com/certification/what-we-certify/enterprise-architect" tooltiptext="Zachman Enterprise Architect Practitioner (Level 2)
    $2,999 exam &amp; case study
    Level 1 cert not req'd" tabindex="0" target="_blank" >Zach EAP</a>
                    <a class="mgmtitem1" href="https://www.giac.org/certification/gslc" tooltiptext="GIAC Security Leadership Certification
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GSLC</a>
                    <a class="mgmtitem1" href="https://www.seco-institute.org/certifications/information-security-certification-track/" tooltiptext="SECO Certified Information Security Officer
    Resume review" tabindex="0" target="_blank" >S-CISO</a>
                    <div class="spacer10"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem2" href="https://www.giac.org/certification/gcfe" tooltiptext="GIAC Cerified Forensics Examiner
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCFE</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certifications/enterprise-incident-responder-geir/" tooltiptext="GIAC Enterprise Incident Response
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GEIR</a>
                    <a class="redopsitem1" href="https://www.pentesteracademy.com/gcb" tooltiptext="Pentester Academy Certified Enterprise Security Specialist
    $339-749 Lab access
    Exam included" tabindex="0" target="_blank" >PACES</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.seco-institute.org/certifications/ethical-hacking-track/leader/" tooltiptext="SECO Certified Ethical Hacker Leader
    Application" tabindex="0" target="_blank" >S-CEHL</a>
                    <a class="redopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-registered-penetration-tester" tooltiptext="CREST Registered Penetration Tester
    $612 exam" tabindex="0" target="_blank" >CREST CRT</a>
                    <a class="redopsitem1" href="https://training.zeropointsecurity.co.uk/courses/red-team-ops-ii" tooltiptext="Zero Point Security Red Team Operator II
    $121 lab" tabindex="0" target="_blank" >CRTO II</a>
                    <a class="redopsitem1" href="https://www.mosse-institute.com/certifications/mcd-certified-code-deobfuscation-specialist.html" tooltipright="Mosse Institute Certified Code Deobfuscation Specialist Certification
    $450 certification programme
    100% practical. No expiry." tabindex="0" target="_blank">MCD</a>
                    <div class="spacer"></div>
                    <!-- Row 11 -->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/professional/ccnp-security-v2.html" tooltipleft="Cisco Certified Network Professional - Security
    ~$1,200 exam" tabindex="0" target="_blank" >CCNP Sec</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://www.identitymanagementinstitute.org/cimp/" tooltiptext="Identify Management Institute Certified Identity Management Professional
    $295 + Membership" tabindex="0" target="_blank" >CIMP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem4x" href="https://www.comptia.org/certifications/comptia-advanced-security-practitioner" tooltiptext="CompTIA Advanced Security Practitioner+
    $509 exam" tabindex="0" target="_blank" ><b>CASP+</b></a>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.giac.org/certification/advanced-smartphone-forensics-gasf" tooltiptext="GIAC Advanced Smartphone Forensics
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GASF</a>
                    <a class="blueopsitem2" href="https://security.ine.com/certifications/ecthp-certification/" tooltiptext="eLearnSecurity Certified Threat Hunting Professional
    $400 lab" tabindex="0" target="_blank" >eCTHP</a>
                    <div class="spacer"></div>
		    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.seco-institute.org/certifications/ethical-hacking-certification-track/" tooltiptext="SECO Ethical Hacker Expert
    TBD (still)
    Being redesigned" tabindex="0" target="_blank" >S-EHE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 12 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.juniper.net/us/en/training/certification/certification-tracks/junos-security-track/?tab=jncip-sec" tooltipleft="Juniper Networks Certified Internet Professional, Security
    $400 exam" tabindex="0" target="_blank" >JNCIP Sec</a>
                    <a class="networkitem1" href="https://www.paloaltonetworks.com/services/education/certification#pcnse" tooltipleft="Palo Alto Networks Certified Network Security Engineer
    $175 exam" tabindex="0" target="_blank" >PCNSE</a>
                    <a class="networkitem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcss_zta" tooltiptext="Fortinet Certified Solution Specialist - Zero Trust Access
    $800 two exams" tabindex="0" target="_blank" >FCSS ZTA</a>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcss_SASE" tooltiptext="Fortinet Certified Solution Specialist - Secure Access Service Edge
    $800 two exams" tabindex="0" target="_blank" >FCSS SASE</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcss_public_cloud_security" tooltiptext="Fortinet Certified Solution Specialist - Public Cloud Security
    $400 exam" tabindex="0" target="_blank" >FCSS PCS</a>
                    <a class="engineeritem1" href="https://www.giac.org/certifications/cloud-threat-detection-gctd/" tooltiptext="GIAC Cloud Threat Detection
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCTD</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.exidacace.com/Apply/CACE" tooltiptext="Excida IEC 62443 Certified Automation Cybersecurity Expert
    $700 exam" tabindex="0" target="_blank" >CACE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem2" href="https://www.axelos.com/certifications/itil-certifications/itil-managing-professional-itil-4" tooltiptext="ITIL Managing Professional
    $9,600 4 course exams
    4 branded courses requires" tabindex="0" target="_blank" >ITIL MP</a>
                    <a class="mgmtitem1" href="https://www.scrum.org/scaled-professional-scrum-certification" tooltiptext="Scrum Scaled Professional Scrum
    $250 exam" tabindex="0" target="_blank" >Scrum SPS</a>
                    <a class="mgmtitem1" href="https://www.giac.org/certification/law-data-security-investigations-gleg" tooltiptext="GIAC Law of Data Security &amp; Investigations
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GLEG</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/information_systems_security/cissm" tooltiptext="GAQM Certified Information Systems Security Manager
    $170 exam" tabindex="0" target="_blank" >CISSM</a>
                    <a class="mgmtitem1" href="https://www.isc2.org/Certifications/CGRC" tooltiptext="(ISC)2 Certified in Governance, Risk and Compliance
    $599 exam" tabindex="0" target="_blank" >CGRC</a>
                    <div class="spacer"></div>
                    <a class="mgmtitem3" href="https://www.isaca.org/credentialing/crisc" tooltiptext="ISACA Certified in Risk and Information Systems Control
    $760 exam" tabindex="0" target="_blank" >CRISC</a>
                    <a class="testitem1" href="https://www.giac.org/certification/critical-controls-certification-gccc" tooltiptext="GIAC Critical Controls Certification
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCCC</a>
                    <a class="testitem1" href="https://www.pcisecuritystandards.org/assessors_and_solutions/become_qsa/" tooltiptext="PCI Qualified Security Assessor
                    $3000 req'd course" tabindex="0" target="_blank" >PCI QSA</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://www.giac.org/certification/certified-web-application-defender-gweb" tooltiptext="GIAC Certified Web Application Defender
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GWEB</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/professional/cyberops-professional.html" tooltiptext="Cisco Certified CyberOps Professional
    $700 two exams" tabindex="0" target="_blank" >Cisco COP</a>
                    <a class="blueopsitem1" href="https://app.infosecinstitute.com/portal/courses/a0t1A000009H5RcQAK" tooltiptext="Infosec Institute Certified Computer Forensics Examiner
    $4,599 exam
    Course required" tabindex="0" target="_blank" >CCFE</a>
                    <a class="blueopsitem2" href="https://www.giac.org/certification/certified-enterprise-defender-gced" tooltiptext="GIAC Certified Enterprise Defender
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCED</a>
                    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mcpe-certified-cyber-protection-expert.html" tooltiptext="Mosse Institute Certified Cyber Protection Expert
    $800 exam" tabindex="0" target="_blank" >MCPE</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-threat-intelligence-manager" tooltiptext="CREST Certified Threat Intelligence Manager
    $2,480 3 exams" tabindex="0" target="_blank" >CREST CCTIM</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem2" href="https://www.offensive-security.com/pwk-oscp/" tooltipright="Offensive Security Certified Professional
    $1,499 labs" tabindex="0" target="_blank" >OSCP</a>
                    <div class="spacer"></div>
                    <!-- Row 13 -->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://view.ceros.com/f5/certification-roadmap/p/9?heightOverride=740" tooltipleft="F5 Big-IP Certified Solution Expert - Security
    $135 exam" tabindex="0" target="_blank" >F5 CSE Sec</a>
                    <a class="networkitem1" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/professional/ccnp-enterprise.html" tooltipleft="Cisco Certified Network Professional - Enterprise
    ~$600 exam" tabindex="0" target="_blank" >CCNP Ent</a>
                    <div class="spacer"></div>
                    <a class="engineeritem2" href="https://docs.microsoft.com/en-us/learn/certifications/m365-enterprise-administrator" tooltiptext="Microsoft 365 Certified Enterprise Administrator Expert
    $165 exam" tabindex="0" target="_blank" >MS-100</a>
                    <a class="engineeritem1" href="https://www.giac.org/certifications/public-cloud-security-gpcs/" tooltiptext="GIAC Public Cloud Security
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GPCS</a>
                    <a class="engineeritem1" href="https://www.giac.org/certification/cloud-security-automation-gcsa" tooltiptext="GIAC Cloud Security Automation
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCSA</a>
                    <a class="engineeritem1" href="https://www.giac.org/certifications/certified-windows-security-administrator-gcwn/" tooltiptext="GIAC Certified Windows Security Administrator
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCWN</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.giac.org/certification/response-industrial-defense-grid" tooltiptext="GIAC Response and Industrial Defense
    $979 exam
    SANS course encouraged" tabindex="0" target="_blank" >GRID</a>
                    <a class="engineeritem1" href="https://www.itgovernance.co.uk/shop/product/certified-iso-27001-isms-lead-implementer-training-course" tooltiptext="IBITGQ Certified ISO 27001 Information Security Management Specialist Lead Implementer
    $2,008 course exam
    Branded course required" tabindex="0" target="_blank" >CIS LI</a>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://iapp.org/certify/cipt/" tooltiptext="IAPP Certified Information Privacy Technologist
    $550 exam" tabindex="0" target="_blank" >CIPT</a>
                    <a class="assetitem2" href="https://www.isaca.org/credentialing/certified-data-privacy-solutions-engineer" tooltiptext="ISACA Certified Data Privacy Solutions Engineer
    $880 Application" tabindex="0" target="_blank" >CDPSE</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/scrum_agile/csm" tooltiptext="GAQM Certified Scrum Master
    $128 exam" tabindex="0" target="_blank" >CSM</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/scrum_agile/casm" tooltiptext="GAQM Certified Agile Scrum Master
    $128 exam" tabindex="0" target="_blank" >CASM</a>
                    <a class="mgmtitem1" href="https://www.mile2.com/master-certifications/" tooltiptext="Mile2 Certified Master Information Systems Security Officer
    Complete C)SP, C)ISSO, C)ISSM and IS20 ($2200)" tabindex="0" target="_blank" >CM)ISSO</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.seco-institute.org/certifications/information-security-certification-track/" tooltiptext="SECO Information Security Practitioner
    $550" tabindex="0" target="_blank" >S-ISP</a>
                    <a class="testitem2" href="https://www.isaca.org/credentialing/cisa" tooltiptext="ISACA Certified Information Systems Auditor
    $760 exam" tabindex="0" target="_blank" >CISA</a>
                    <a class="testitem1" href="https://www.giac.org/certification/continuous-monitoring-certification-gmon" tooltiptext="GIAC Continuous Monitoring
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GMON</a>
                    <a class="testitem1" href="https://www.itgovernance.co.uk/shop/product/certified-iso-27001-isms-lead-auditor-training-course" tooltiptext="IBITGQ Certified ISO 27001 Information Security Management Specialist Lead Auditor
    $2,008 course exam
    Branded course required" tabindex="0" target="_blank" >CIS LA</a>
                    <div class="spacer"></div><a class="softwareitem1" href="https://www.seco-institute.org/certifications/certified-secure-software-developer/" tooltiptext="SECO Secure Programming Certified Leader
    $460 exam" tabindex="0" target="_blank" >S-CSPL</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.giac.org/certification/certified-detection-analyst-gcda" tooltiptext="GIAC Certified Detection Analyst
        $979 exam
        SANS course recommended" tabindex="0" target="_blank">GCDA</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://app.infosecinstitute.com/portal/courses/a0t1A000009H6juQAC" tooltiptext="Infosec Institute Certified Mobile Forensics Examiner
    $1,699 exam
    Course required" tabindex="0" target="_blank" >CMFE</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certifications/experienced-forensics-analyst-gxfa/" tooltiptext="GIAC Experienced Forensics Analyst
    $1299 exam
    SANS course recommended" tabindex="0" target="_blank" >GX-FA</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem2" href="https://www.giac.org/certification/gcih" tooltiptext="GIAC Certified Forensics Analystr
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCIH</a>
                    <a class="redopsitem1" href="https://www.giac.org/certifications/experienced-penetration-tester-gxpt/" tooltiptext="GIAC Experienced Penetration Tester
    $1299 exam
    SANS course recommended" tabindex="0" target="_blank" >GX-PT</a>
                    <a class="redopsitem1" href="https://www.giac.org/certification/gpen" tooltiptext="GIAC Certified Penetration Tester
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GPEN</a>
                    <a class="redopsitem1" href="https://www.offensive-security.com/wifu-oswp/" tooltiptext="Offensive Security Wireless Professional
    $450 labs" tabindex="0" target="_blank" >OSWP</a>
                    <a class="redopsitem1" href="https://courses.zeropointsecurity.co.uk/courses/red-team-ops" tooltipright="Zero Point Security Certified Red Team Operator
    $121 lab" tabindex="0" target="_blank" >CRTO</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 14 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://training-certifications.checkpoint.com/#/courses/Check%20Point%20Certified%20Master%20(CCSM)%20R80.x" tooltipleft="Checkpoint Certified Security Master
    $350 exam" tabindex="0" target="_blank" >CCSM</a>
                    <a class="networkitem1" href="https://www.paloaltonetworks.com/services/education/certification" tooltipleft="Palo Alto Certified Cloud Security Automation Engineer
    $350 exam" tabindex="0" target="_blank" >PCSAE</a>
                    <a class="networkitem1" href="https://www.paloaltonetworks.com/services/education/certification" tooltipleft="Prisma Certified Cloud Security Engineer
    $350 exam" tabindex="0" target="_blank" >PCCSE</a>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://www.identitymanagementinstitute.org/ciam/" tooltiptext="Identify Management Institute Certified Identify and Access Manager
    $390 Exam" tabindex="0" target="_blank" >CIAM</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcss_security_operations" tooltiptext="Fortinet Certified Solution Specialist - Security Operations
    $400 exam" tabindex="0" target="_blank" >FCSS SO</a>
                    <a class="engineeritem1" href="https://www.practical-devsecops.com/certified-devsecops-expert" tooltiptext="PDSO Certified DevSecOps Expert
    $1199
    Exam and training bundled" tabindex="0" target="_blank" >PDSO CDE</a>
                    <a class="engineeritem1" href="https://www.vmware.com/education-services/certification/vcp-dcv.html" tooltiptext="VMware Certified Professional in Datacenter Virtualization
    $375 exam
    Branded course required" tabindex="0" target="_blank" >VCP DCV</a>
                     <a class="engineeritem1" href="https://www.cncf.io/certification/cks/" tooltiptext="Cloud Native Computing Foundation Certified Kubernetes Security Specialist
    $375 lab
    Branded course required" tabindex="0" target="_blank" >CKS</a>
                            <a class="engineeritem1" href="https://training.linuxfoundation.org/certification/linux-foundation-certified-sysadmin-lfcs/" tooltiptext="Linux Foundation Certified System Administrator
    $300 exam" tabindex="0" target="_blank" >LFCS</a>
                    <a class="engineeritem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcss_ot_security" tooltiptext="Fortinet Certified Solution Specialist - OT Security
    $400 exam" tabindex="0" target="_blank" >FCSS OT</a>
                    <a class="engineeritem4" href="https://app.infosecinstitute.com/portal/courses/a0tC0000000Fp4JIAS" tooltiptext="Infosec Institute Certified SCADA Security Architect
    $4,599 exam
    Course required" tabindex="0" target="_blank" >CSSA</a>
                    <a class="mgmtitem1" href="https://www.scrum.org/professional-scrum-developer-certification" tooltiptext="Scrum Professional Scrum Developer
    $200 exam" tabindex="0" target="_blank" >Scrum PSD</a>
                    <a class="mgmtitem1" href="https://www.giac.org/certification/gcpm" tooltiptext="GIAC Certified Project Manager
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCPM</a>
                    <a class="mgmtitem1" href="https://www.bcs.org/get-qualified/certifications-for-professionals/information-security-and-ccp-scheme-certifications/bcs-practitioner-certificate-in-information-risk-management/" tooltiptext="BCS Practitioner Certificate in Information Risk Management
    $287 exam" tabindex="0" target="_blank" >BCS PCIRM</a>
                    <a class="mgmtitem1" href="https://www.exin.com/certifications/information-security-management-professional-based-isoiec-27001-exam" tooltiptext="EXIN Information Security Management Professional
    $268 exam" tabindex="0" target="_blank" >PEXIN ISM</a>
                    <a class="mgmtitem1" href="https://www.mosse-institute.com/certifications/mgrc-certified-grc-practitioner.html" tooltiptext="Mosse Institute Certified GRC Expert Certification
  $450 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MGRC</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="softwareitem6" href="https://www.isc2.org/Certifications/CSSLP" tooltiptext="(ISC)2 Certified Secure Software Lifecycle Professional
    $599 exam" tabindex="0" target="_blank" >CSSLP</a>
                    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mth-certified-threat-hunter.html" tooltiptext="Mosse Institute Certified Threat Hunter Certification
                    $450 certification programme
                    100% practical. No expiry." tabindex="0" target="_blank">MTH</a>
                    <a class="blueopsitem1" href="https://app.infosecinstitute.com/portal/courses/a0tC0000000FovhIAC" tooltiptext="Infosec Institute Certified Data Recovery Professional
    $4,599 exam
    Course required" tabindex="0" target="_blank" >CDRP</a>
                    <a class="blueopsitem1" href="https://security.ine.com/certifications/ecdfp-certification/" tooltiptext="eLearnSecurity Certified Digital Forensics Professional
    $400 exam" tabindex="0" target="_blank" >eCDFP</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certification/python-coder-gpyc" tooltiptext="GIAC Python Coder
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GPYC</a>
                    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mdfir-certified-dfir-specialist.html" tooltiptext="Mosse Institute Certified DFIR Specialist
  $450 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MDFIR</a>
                    <a class="redopsitem1" href="https://www.eccouncil.org/programs/licensed-penetration-tester-lpt-master/" tooltiptext="EC Council Licensed Penetration Tester
    $899 exam" tabindex="0" target="_blank" >LPT</a>
                    <a class="redopsitem1" href="https://certifications.tcm-sec.com/pnpt/" tooltiptext="TCM Security Practical Network Penetration Tester
    $299 exam" tabindex="0" target="_blank" >PNPT</a>
                    <a class="redopsitem1" href="https://www.giac.org/certification/gcpn" tooltiptext="GIAC Cloud Penetration Tester
    $2,499 exam
    SANS course recommended" tabindex="0" target="_blank" >GCPN</a>
                     <a class="redopsitem1" href="https://www.giac.org/certifications/red-team-professional-grtp/" tooltiptext="GIAC Red Team Professional
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GRTP</a>
                    <a class="redopsitem1" href="https://secops.group/product/certified-appsec-pentesting-expert-capenx/" tooltiptext="The SecurityOps Group Certified AppSec Pentesting eXpert
    $800 exam" tabindex="0" target="_blank" >SOG CAPenX</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.giac.org/certification/mobile-device-security-analyst-gmob" tooltipright="GIAC Mobile Device Security Analyst
    $399 exam
    SANS course recommended" tabindex="0" target="_blank" >GMOB</a>
                    <!-- Row 15 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcss_network_security" tooltipleft="Fortinet Certificed Solution Specialist - Network Security
    $800 two exams" tabindex="0" target="_blank" >FCSS NS</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://idpro.org/cidpro/" tooltiptext="IDPro Certified Identity Professional
    $700 exam" tabindex="0" target="_blank" >CIDPRO</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.isc2.org/Certifications/CCSP" tooltiptext="(ISC)2 Certified Cloud Security Professional
    $599 exam" tabindex="0" target="_blank" >CCSP</a>
                    <a class="engineeritem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcp_public_cloud_security" tooltipleft="Fortinet Certified Professional - Public Cloud Security
    $400 for 2 exams" tabindex="0" target="_blank" >FCP PCS</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcp_security_operations" tooltipleft="Fortinet Certified Professional - Security Operations
    $400 for 2 exams" tabindex="0" target="_blank" >FCP SO</a>
                    <a class="engineeritem1" href="https://www.redhat.com/en/services/certification/rhcsa" tooltiptext="Red Hat Certified System Administrator
    $400 exam" tabindex="0" target="_blank" >RHCSA</a>
                    <a class="engineeritem1" href="https://www.isa.org/training-and-certifications/isa-certification/isa99iec-62443/isa99iec-62443-cybersecurity-certificate-programs/" tooltiptext="ISA Certified Design Specialist
    $2,700 course + exam" tabindex="0" target="_blank" >ISA CDS</a>
                    <a class="engineeritem1" href="https://trailhead.salesforce.com/help?article=Salesforce-Certified-Technical-Architect-Exam-Guide" tooltiptext="Salesforce Certified Technical Architect
    $6000
    Must be SF SA Certified" tabindex="0" target="_blank">SFCTA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://embed.exin.totalservices.io/certifications/exin-privacy-and-data-protection-practitioner-exam" tooltiptext="EXIN Privacy and Data Protection Practitioner
    $243 Exam
    Course req'd" tabindex="0" target="_blank" >EPDPP</a>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.axelos.com/certifications/propath/mor-risk-management/mor-4-practitioner" tooltiptext="Axelos M_o_R Practitioner Risk Management
    $560 exam" tabindex="0" target="_blank" >M_o_R P</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/project_management/cpd" tooltiptext="GAQM Certified Project Director
    $210 exam" tabindex="0" target="_blank" >CPD</a>
                    <a class="mgmtitem1" href="https://www.pmi.org/certifications/types/agile-acp" tooltiptext="PMI Agile Certified Practitioner
    $495 exam" tabindex="0" target="_blank" >PMI ACP</a>
                    <a class="mgmtitem1" href="https://ciso.eccouncil.org/cciso-certification/eism-program/" tooltiptext="EC Council Information Security Manager
    $3,499
    Branded course required" tabindex="0" target="_blank" >EISM</a>
                    <a class="mgmtitem1" href="https://www.isaca.org/credentialing/cgeit" tooltiptext="ISACA Certified in the Governance of Enterprise IT
    $760 exam" tabindex="0" target="_blank" >CGEIT</a>
                    <a class="mgmtitem1" href="https://www.exin.com/certifications/information-security-management-expert-based-isoiec-27001-exam?language_content_entity=en" tooltiptext="EXIN ISO/IEC 27001 Expert
    ~$379 Oral Presentation" tabindex="0" target="_blank" >EXIN 27001E</a>
                    <a class="mgmtitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27005/iso-27005-lead-risk-manager" tooltiptext="PECB ISO/IEC 27005 Lead Risk Manager
    ~$1,595 exam
    Course required" tabindex="0" target="_blank" >PECB 27005LM</a>
                    <a class="mgmtitem1" href="https://drii.org/certification/ccrp" tooltiptext="DRI Certified Cyber Resilience Professional
    $400 Exam" tabindex="0" target="_blank" >DCCRP</a>
                    <a class="testitem2" href="https://www.giac.org/certification/certified-intrusion-analyst-gcia" tooltiptext="GIAC Certified Intrusion Analyst
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GCIA</a>
                    <a class="testitem1" href="https://sharedassessments.org/ctpra/" tooltiptext="Shared Assessment Certified Third-Party Risk Assessor
    $1295 course" target="_blank">CTPRA</a> 
                    <a class="testitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27001/iso-iec-27001-lead-auditor" tooltiptext="PECB ISO/IEC 27001 Lead Auditor
    $930 exam
    Course required" tabindex="0" target="_blank" >PECB 27001LA</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://www.cisco.com/site/us/en/learn/training-certifications/certifications/devnet/professional/index.html" tooltiptext="Cisco DevNet Professional
    $1200 two exams
    DevNet Associate req'd" tabindex="0" target="_blank" >DevNet Pro</a>
                     <div class="spacer"></div>
                     <a class="blueopsitem1" href="https://docs.microsoft.com/en-us/learn/certifications/information-protection-administrator/" tooltiptext="Microsoft Certified Information Protection Administrator Associate
    $165 exam" tabindex="0" target="_blank" >SC-400</a>
                    <a class="blueopsitem1" href="https://www.isfce.com/certification.htm" tooltiptext="ISFCE Certified Computer Examiner
    $485 written exam" tabindex="0" target="_blank" >CCE</a>
                    <a class="blueopsitem1" href="https://www.mile2.com/master-certifications/" tooltiptext="Mile2 Certified Master Digital Forensic Investigator
    Complete C)SP, C)DFE, C)NFE and C)CSA ($2200)" tabindex="0" target="_blank" >CM)DFI</a>
                    <a class="blueopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-registered-intrusion-analyst" tooltiptext="CREST Registered Intrusion Analyst
    $612 exam &amp; lab" tabindex="0" target="_blank" >CREST CRIA</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-registered-threat-intelligence-analyst" tooltiptext="CREST Registered Threat Intelligence Analyst
    $615 2 exams" tabindex="0" target="_blank" >CREST CRTIA</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.giac.org/certification/gwapt" tooltiptext="GIAC Web Application Penetration Tester
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GWAPT</a>
                    <a class="redopsitem1" href="https://www.offensive-security.com/exp312-osmr/" tooltiptext="Offensive Security MacOS Researcher
    $2,499 exam
    Learning subscription required" tabindex="0" target="_blank" >OSMR</a>
                    <a class="redopsitem1" href="https://gaqm.org/certifications/information_systems_security/certified_penetration_tester_cpt" tooltiptext="GAQM Certified Penetration Tester
    $128 exam" tabindex="0" target="_blank" >GCPT</a>
                    <a class="redopsitem1" href="https://secops.group/product/certified-cloud-pentesting-expert/" tooltiptext="The SecurityOps Group Certified Cloud Pentesting eXpert-AWS
    $800 exam" tabindex="0" target="_blank" >CCPenX-AWS</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 16 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://training-certifications.checkpoint.com/#/courses/Check%20Point%20Certified%20Expert%20(CCSE)%20R80.x" tooltipleft="Checkpoint Certified Security Expert
    $250 exam" tabindex="0" target="_blank" >CCSE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem2" href="https://aws.amazon.com/certification/certified-security-specialty/" tooltiptext="Amazon Web Services Certified Security - Specialty
    $150 exam" tabindex="0" target="_blank" >AWS CSS</a>
                    <a class="engineeritem1" href="https://trailhead.salesforce.com/help?article=Salesforce-Certified-Community-Cloud-Consultant-Exam-Guide" tooltiptext="SalesForce Certified Community Cloud Consultant
    $200 exam
    Must be SalesForce Admin Certified" tabindex="0" target="_blank">SFCCCC</a>
                    <a class="engineeritem1" href="https://www.exin.com/certifications/ccc-professional-cloud-solution-architect-exam" tooltiptext="EXIN Professional Cloud Solution Architect
    $315 exam" tabindex="0" target="_blank" >EXIN PCSA</a>
                    <a class="engineeritem1" href="https://www.cncf.io/certification/cka/" tooltiptext="Cloud Native Computing Foundation Certified Kubernetes Administrator
    $375 lab
    Branded course required" tabindex="0" target="_blank" >CKA</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.tuv.com/landingpage/en/lp-certified-operational-technology-cybersecurity-professional-program/" tooltiptext="TUV Rheinland Certified Operational Technology Cybersecurity Professional (GERMAN)
                        $415 exam" tabindex="0" target="_blank" >TUV COTCP</a>
                    <a class="engineeritem1" href="https://sabsa.org/certification/" tooltiptext="SABSA Chartered Security Architect - Foundation Certificate
    $3,750 exam
    Branded course required" tabindex="0" target="_blank" >SABSA SCF</a>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://www.identitymanagementinstitute.org/cipa/" tooltiptext="IMI Certified Identity Protection comptia-advanced-security-practitioner
    $295 Exam" tabindex="0" target="_blank" >CIPA</a>
                    <a class="assetitem1" href="https://www.dsci.in/content/dsci-certified-privacy-professional-dcpp" tooltiptext="DSCI Certified Privacy Professional
    $205 Exam" tabindex="0" target="_blank" >DCPP</a>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.scrum.org/professional-agile-leadership-certification" tooltiptext="Scrum  Professional Agile Leadership
    $200 exam" tabindex="0" target="_blank" >Scrum PAL</a>
                    <a class="mgmtitem1" href="https://www.pmi.org/certifications/types/certified-associate-capm" tooltiptext="PMI Certified Associate in Project Management
    $300 exam" tabindex="0" target="_blank" >CAPM</a>
                    <a class="mgmtitem1" href="https://www.scrum.org/assessments/professional-scrum-master-ii-certification" tooltiptext="Scrum.org Professional Scrum Master II
    $250 exam" tabindex="0" target="_blank" >PSM II</a>
                    <a class="mgmtitem1" href="https://apmg-international.com/product/iso-iec-20000" tooltiptext="APMG ISO/IEC 20000 Practitioner
    $308 Exam
    Foundation or ITIL req'd">APMG 20000P</a>
                    <a class="mgmtitem1" href="https://www.mile2.com/information-systems-risk-mangager-outline/" tooltiptext="Mile2 Certified Information Systems Risk Manager
    $550 exam" tabindex="0" target="_blank" >C)ISRM</a>
                    <a class="mgmtitem1" href="https://apmg-international.com/product/isoiec-27001" tooltiptext="APMG ISO/IEC 27001 Practitioner
    $400 exam
    Application essay" tabindex="0" target="_blank" >APMG 27001P</a>
                    <a class="mgmtitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27001/iso-iec-27001-lead-implementer" tooltiptext="PECB ISO/IEC 27001 Lead Implementer
    $930 exam
    Course required" tabindex="0" target="_blank" >PECB 27001LI</a>
                    <div class=""spacer"></div>
                    <a class="testitem2" href="https://www.mile2.com/is20_outline/" tooltiptext="Mile2 IS20 Controls
    $550 exam" tabindex="0" target="_blank" >IS20</a>
                    <a class="testitem1" href="https://www.mile2.com/information_systems_security_auditor_outline/" tooltiptext="Mile2 Certified Information Systems Security Auditor
    $550 exam" tabindex="0" target="_blank" >C)ISSA</a>
                    <a class="testitem1" href="https://apmg-international.com/product/isoiec-27001" tooltiptext="APMG ISO/IEC 27001 Auditor
    $400 exam
    Application essay" tabindex="0" target="_blank" >APMG 27001A</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://www.eccouncil.org/programs/certified-application-security-engineer-case/" tooltiptext="EC Council Certified Application Security Engineer (.NET or Java)
    $550 exam" tabindex="0" target="_blank" >CASE</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.mile2.com/cdre_outline/" tooltiptext="Mile2 Certified Disaster Recovery Engineer
                    $550 exam" tabindex="0" target="_blank" >C)DRE</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certifications/security-operations-certified-gsoc/" tooltiptext="GIAC Security Operations Certified
    $979 exam
    SANS course recommended" tabindex="0" target="_blank">GSOC</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certification/gbfa" tooltiptext="GIAC Battlefield Forensics and Acquisition
    $979 exam
    SANS course recommended" tabindex="0" target="_blank">GBFA</a>
                    <a class="blueopsitem2" href="https://www.securityblue.team/why-btl1/" tooltiptext="Security Blue Team Level 1
    $660 course
    1 exam attempt included" tabindex="0" target="_blank">BTL1</a>
                    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mbt-certified-blue-teamer.html" tooltiptext="Mosse Institute Certified Blue Teamer Certification
  $450 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MBT</a>
                    <a class="redopsitem1" href="https://www.mosse-institute.com/certifications/mpt-certified-penetration-tester.html" tooltiptext="Mosse Institute Certified Penetration Tester Certification
    $450 certification programme
    100% practical. No expiry." tabindex="0" target="_blank">MPT</a>
                    <a class="redopsitem1" href="https://www.eccouncil.org/programs/certified-penetration-testing-professional-cpent/" tooltiptext="EC Council Certified Penetration Testing Professional
    $999 exam" tabindex="0" target="_blank" >CPENT</a>
                    <a class="redopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-web-application-tester/" tooltiptext="CREST Certified Web Application Tester
    $2,520 exam &amp; lab" tabindex="0" target="_blank" >CREST CCTAPP</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://academy.hackthebox.com/preview/certifications/htb-certified-penetration-testing-specialist/" tooltiptext="Hack the Box Certified Penetration Testing Specialist
    $200 modules + $210 exam
    $490 Subscription available" tabindex="0" target="_blank" >HTB CPTS</a>
                    <a class="redopsitem1" href="https://www.mosse-institute.com/certifications/mre-certified-reverse-engineer.html" tooltipright="Mosse Institute Certified Reverse Engineer Certification
    $450 certification programme
    100% practical. No expiry." tabindex="0" target="_blank">MRE</a>
                    <div class="spacer"></div>
                    <!-- Row 17 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.juniper.net/us/en/training/certification/certification-tracks/junos-security-track/?tab=jncisec" tooltipleft="Juniper Networks Certified Internet Specialist, Security
    $300 exam" tabindex="0" target="_blank" >JNCIS Sec</a>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem4x" href="https://www.learnpython.org/" tooltiptext="Learning a programming language is valuable to any IT professionals career.
    Recommendations: Python, Ruby, C++" tabindex="0" target="_blank" ><b>Programming Language</b></a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://www.giac.org/certifications/machine-learning-engineer-gmle/" tooltiptext="GIAC Machine Learning Engineer
    $979 exam" tabindex="0" target="_blank" >GMLE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-host-intrusion-analyst" tooltiptext="CREST Certified Host intrustion Analyst
    $2,481 exam &amp; essay
    Hands on exam in UK" tabindex="0" target="_blank" >CREST CCHIA</a>
                    <a class="blueopsitem1" href="https://www.opentext.com/products-and-solutions/services/training-and-learning-services/encase-training/examiner-certification" tooltiptext="OpenText EnCase Certified Examiner
    $200 two exams" tabindex="0" target="_blank" >EnCE</a>
                    <a class="blueopsitem1" href="https://accessdata.com/training/computer-forensics-certification" tooltiptext="AccessData Certified Examiner
    $100 + software" tabindex="0" target="_blank" >ACE</a>
                    <a class="blueopsitem1" href="https://security.ine.com/certifications/ecir-certification/" tooltiptext="eLearnSecurity Certified Incident Responder
    $400 lab" tabindex="0" target="_blank" >eCIR</a>
                    <a class="blueopsitem1" href="https://www.mile2.com/cihe_outline/" tooltiptext="Mile2 Certified Incident Handling Engineer
    $550 exam" tabindex="0" target="_blank" >C)IHE</a>
    <a class="redopsitem1" href="https://thecyberscheme.org/cyber-scheme-team-leader-cstl-exam/" tooltiptext="Cyber Scheme Team Leader
    $1945 exam" tabindex="0" target="_blank" >CSTL</a>
                    <a class="redopsitem1" href="https://security.ine.com/certifications/ecppt-certification/" tooltiptext="eLearnSecurity Certified Professional Penetration Tester
    $400 lab" tabindex="0" target="_blank" >eCPPT</a>
                    <a class="redopsitem1" href="https://security.ine.com/certifications/ewpt-certification/" tooltiptext="eLearnSecurity Web Application Penetration Tester
    $400 lab" tabindex="0" target="_blank" >eWPT</a>
                    <a class="redopsitem1" href="https://www.mile2.com/master-certifications/" tooltiptext="Mile2 Certified Master Intrusion Prevention Specialist
    Complete C)VA, C)PEH, C)PTE and C)PTC ($2200)" tabindex="0" target="_blank" >CM)IPS</a>
                    <a class="redopsitem1" href="https://academy.hackthebox.com/preview/certifications/htb-certified-bug-bounty-hunter/" tooltiptext="Hack the Box Certified Bug Bounty Hunter
    $145 modules + $210 exam
    $490 Subscription available" tabindex="0" target="_blank" >HTB CBBH</a>
                    <a class="redopsitem1" href="https://certifications.tcm-sec.com/pjmr/" tooltipright="Practical Junior Malware Researcher
    $399 lab" tabindex="0" target="_blank" >PJMR</a>
                    <div class="spacer"></div>
                    <!-- Row 18 -->
                    <div class="skilllevelitem"><span style="color:var(--orangedk)">Intermediate</span></div>
                    <a class="networkitem1" href="https://view.ceros.com/f5/certification-roadmap/p/9?heightOverride=740" tooltipleft="F5 Big-IP Certified Technical Specialist - Access Policy Manager
    $135 exam" tabindex="0" target="_blank" >F5 CTS APM</a>
                    <a class="networkitem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcp_network_security" tooltipleft="Fortinet Certified Professional - Network Security
    $400 for 2 exams" tabindex="0" target="_blank" >FCP NS</a>
                    <a class="networkitem1" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/associate/ccna.html" tooltiptext="Cisco Certified Network Associate
    ~$330 exam" tabindex="0" target="_blank" >CCNA</a>
                    <div class="spacer"></div>
                    <a class="engineeritem2" href="https://docs.microsoft.com/en-us/learn/certifications/azure-security-engineer?wt.mc_id=learningredirect_certs-web-wwl" tooltiptext="Microsoft Azure Security Engineer Associate
    $165 exam" tabindex="0" target="_blank" >AZ-500</a>
                    <a class="engineeritem1" href="https://cloudsecurityalliance.org/education/cloud-governance-and-compliance/" tooltiptext="Cloud Security Alliance Cloud Governance &amp; Compliance
    $315 exam" tabindex="0" target="_blank" >CSA CGC</a>
                    <a class="engineeritem1" href="https://www.vmware.com/education-services/certification/vcp-nv-tracks.html" tooltiptext="VMware Certified Professional in Network Virtualization
    $375 exam
    Branded course required" tabindex="0" target="_blank" >VCP NV</a>
                    <a class="engineeritem1" href="https://www.cncf.io/certification/ckad/" tooltiptext="Cloud Native Computing Foundation Certified Kubernetes Application Developer
    $375 lab
    Branded course required" tabindex="0" target="_blank" >CKAD</a>
                    <a class="engineeritem1" href="https://www.lpi.org/our-certifications/lpic-2-overview" tooltiptext="Linux Professional Institute Certified: Linux Engineer
    $400 2 exams" tabindex="0" target="_blank" >LPIC-2</a>
                    <a class="engineeritem1" href="https://www.giac.org/certification/critical-infrastructure-protection-gcip" tooltiptext="GIAC Critical Infrastructure Protection
    $979 exam
    SANS course encouraged" tabindex="0" target="_blank" >GCIP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://www.identitymanagementinstitute.org/cimp/" tooltiptext="IMI Certified Identity Management Professional
    $295 Exam" tabindex="0" target="_blank" >CIMP</a>
                    <a class="assetitem2" href="https://www.identitymanagementinstitute.org/cdp/" tooltiptext="IMI Certified in Data Protection
    $395 Exam" tabindex="0" target="_blank" >CDP</a>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://ecfirst.biz/index.php?route=product/product&path=59_83&product_id=281" tooltiptext="EC First Certified CCMC Professional
    $2,995 exam
    Course required" tabindex="0" target="_blank" >CCP</a>
                    <a class="mgmtitem1" href="https://www.mile2.com/cisso_outline/" tooltiptext="Mile2 Certified Information Systems Security Officer
    $550 exam" tabindex="0" target="_blank" >C)ISSO</a>
                    <a class="mgmtitem1" href="https://www.itgovernance.co.uk/shop/product/iso-27005-certified-isms-risk-management" tooltiptext="IBITGQ Certified ISO 27005 Information Security Management Specialist Risk Management
    $2,783 course exam
    Branded course required" tabindex="0" target="_blank" >CIS RM</a>
                    <a class="mgmtitem1" href="https://www.exin.com/certifications/information-security-management-professional-based-isoiec-27001-exam" tooltiptext="EXIN ISO/IEC 27001 Professional
    $279 exam" tabindex="0" target="_blank" >EXIN 27001P</a>
                    <a class="mgmtitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27032/iso-iec-27032-lead-cyber-security-manager" tooltiptext="PECB ISO/IEC 27032 Lead Cybersecurity Manager
    $899-$2,999 course exam
    Course required" tabindex="0" target="_blank" >PECB 27032CM</a>
                    <a class="mgmtitem1" href="https://www.mile2.com/chissp_outline/" tooltiptext="Mile2 Certified Healthcare Information Systems Security Practitioner
    $550 exam" tabindex="0" target="_blank" >C)HISSP</a>
                    <a class="testitem2" href="https://apmg-international.com/product/iso-iec-20000" tooltiptext="APMG ISO/IEC 20000 Auditor
    $308 Exam
    Possible Course Req" tabindex="0" target="_blank" >APMG 20000A</a>
                    <a class="testitem1" href="https://www.mile2.com/cisms-la-li-outline/" tooltiptext="Mile2 Certified Information security Management Systems Lead Auditor
    $550 exam" tabindex="0" target="_blank" >C)ISMS-LA</a>
                    <a class="testitem1" href="https://www.itgovernance.co.uk/shop/product/iso27001-certified-isms-internal-auditor-training-course" tooltiptext="IBITGQ Certified ISO 27001 Information Security Management Specialist Internal Auditor
    $1543 course exam
    Branded course required" tabindex="0" target="_blank" >CIS IA</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://gaqm.org/certifications/software_security_testing/casst" tooltiptext="GAQM Certified Advanced Software Security Tester
    $210 exam" tabindex="0" target="_blank" >CASST</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://inteltechniques.com/training-osip.html" tooltiptext="IntelTechniques Open Source Intelligence Professional
    $300 practical exam" tabindex="0" target="_blank" >OSIP</a>
                    <a class="blueopsitem1" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/associate/cyberops-associate.html" tooltiptext="Cisco Certified CyberOps Associate Cyber Operations
    ~$325 exam" tabindex="0" target="_blank">Cisco COA</a>
                    <a class="blueopsitem1" href="https://www.mile2.com/ccsa_outline/" tooltiptext="Mile2 Certified Cybersecurity Analyst
    $550 exam" tabindex="0" target="_blank" >C)CSA</a>
                    <a class="blueopsitem1" href="https://www.eccouncil.org/programs/computer-hacking-forensic-investigator-chfi/" tooltiptext="EC Council Computer Hacking Forensics Investigator
    $650 exam" tabindex="0" target="_blank" >CHFI</a>
                    <a class="blueopsitem1" href="https://www.seco-institute.org/get-trained/cyber-defense-track/threat-analyst-certification/" tooltiptext="SECO Certified Threat Analyst
    $550 exam" tabindex="0" target="_blank" >S-TA</a>
                    <a class="blueopsitem1" href="https://www.eccouncil.org/programs/ec-council-certified-incident-handler-ecih/" tooltiptext="EC Council Certified Incident Handler
    $300 exam" tabindex="0" target="_blank" >ECIH</a>
                    <a class="redopsitem1" href="https://www.mile2.com/cpSH_outline/" tooltiptext="Mile2 Certified Powershell Hacker
    $550 exam" tabindex="0" target="_blank" >C)PSH</a>
                    <a class="redopsitem1" href="https://app.infosecinstitute.com/portal/courses/a0tC0000000Fow6IAC" tooltiptext="Infosec Institute Certified Mobile and Web App Penetration Tester
    $4,599 exam
    Course required" tabindex="0" target="_blank"  style="font-size: 0.5vmax">CMWAPT</a>
                    <a class="redopsitem1" href="https://mile2.com/cptc_outline/" tooltiptext="Mile2 Certified Penetration Testing Consultant
    $550 exam" tabindex="0" target="_blank" >C)PTC</a>
                    <a class="redopsitem1" href="https://app.infosecinstitute.com/portal/courses/a0t0y00000BK8IcAAL" tooltipright="Infosec Institute Certified Red Team Operations Professional
    $4,599 exam
    Course required" tabindex="0" target="_blank" >CRTOP</a>
                    <a class="redopsitem2" href="https://cyberstruggle.org/ranger-certification/" tooltiptext="Cyber Struggle Ranger
    Location Based Cost
    Course Req" tabindex="0" target="_blank" >CSR</a>
                    <div class="spacer"></div>
                    <!-- Row 19 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://view.ceros.com/f5/certification-roadmap/p/9?heightOverride=740" tooltipleft="F5 Big-IP Certified Technical Specialist - Domain Name Services
    $135 exam" tabindex="0" target="_blank" >F5 CTS DNS</a>
                    <a class="networkitem1" href="https://www.paloaltonetworks.com/services/education/certification" tooltiptext="Palo Alto Networks Certified Detection and Remediation Analyst
    $155 exam" tabindex="0" target="_blank" >PCDRA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://trailhead.salesforce.com/help?article=Salesforce-Certified-Identity-and-Access-Management-Designer-Exam-Guide" tooltiptext="SalesForce Certified Identity and Access Management Designer
    $400 exam" tabindex="0" target="_blank">SF CIAMD</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.giac.org/certifications/cloud-security-essentials-gcld/" tooltiptext="GIAC Cloud Security Essentials
    $979 exam SANS course recommended" tabindex="0" target="_blank" >GCLD</a>
                    <a class="engineeritem1" href="https://aws.amazon.com/certification/certified-solutions-architect-associate/" tooltiptext="Amazon Web Services Certified Solutions Architect - Associate
    $150 exam" tabindex="0" target="_blank" >AWS SAA</a>
                    <a class="engineeritem1" href="https://www.exin.com/certifications/ccc-professional-cloud-service-manager-exam" tooltiptext="EXIN Professional Cloud Service Manager
    $315 exam" tabindex="0" target="_blank" >EXIN PCSerM</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.isa.org/training-and-certifications/isa-certification/isa99iec-62443/isa99iec-62443-cybersecurity-certificate-programs/" tooltiptext="ISA Certified Risk Assesment Specialist
    $2,700 course + exam
    Course required" tabindex="0" target="_blank" >ISA CRAS</a>
                    <a class="engineeritem1" href="https://www.splunk.com/en_us/training/certification-track/splunk-es-certified-admin.html" tooltiptext="Splunk Enterprise Security Certified Administrator
    $130 exam
    Branded course recommended" tabindex="0" target="_blank" >SPLK-<wbr/>3001</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem2" href="https://www.bcs.org/get-qualified/certifications-for-professionals/information-security-and-ccp-scheme-certifications/bcs-practitioner-certificate-in-information-assurance-architecture/" tooltiptext="BCS Practitioner Certificate in Information Assurance Architecture
    $290 exam" tabindex="0" target="_blank" >BCS PCIAA</a>
                    <a class="mgmtitem1" href="https://ecfirst.biz/index.php?route=product/product&path=59_61&product_id=77" tooltiptext="EC First Certified Cyber Security Architect
    $695 exam" tabindex="0" target="_blank" >CCSA</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/project_management/ppm" tooltiptext="GAQM Professional in Project Management
    $210 exam" tabindex="0" target="_blank" >PPM</a>
                    <a class="mgmtitem1" href="https://mile2.com/cissm_outline/" tooltiptext="Mile2 Certified Information Systems Security Manager
    $550 exam" tabindex="0" target="_blank" >C)ISSM</a>
                    <a class="mgmtitem1" href="https://www.certipedia.com/quality_marks/0000063483?locale=en" tooltiptext="TUV IT Security Manager (GERMAN)
    $415 exam
    Course required" tabindex="0" target="_blank" >TUV ITSM</a>
                    <a class="mgmtitem1" href="https://www.itgovernance.co.uk/shop/product/managing-cyber-security-risk-training-course" tooltiptext="IBITGQ Certified in Managing Cyber Security Risk
    $2,629 course exam
    Branded course required" tabindex="0" target="_blank" >CCRMP</a>
                    <a class="mgmtitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27005/iso-iec-27005-risk-manager" tooltiptext="PECB ISO/IEC 27005 Risk Manager
    ~$995 exam
    Course required" tabindex="0" target="_blank" >PECB 27005RM</a>
                    <a class="mgmtitem1" href="https://www.softwarecertifications.org/csba/" tooltiptext="QAI Certified Software Business Analyst
    $350 exam + written essay" target="_blank">CSBA</a>
                    <a class="testitem2" href="https://drii.org/certification/cbcla" tooltiptext="DRI Certified Business Continuity Lead Auditor
    $400 exam
    Application req" target="_blank">DCBCLA</a>
                    <a class="testitem1" href="https://www.certipedia.com/quality_marks/0000046324?locale=en" tooltiptext="TUV Rheinland Mobile Security Analyst (GERMAN)
    $415 exam
    Course required" tabindex="0" target="_blank" >TUV MSA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://www.cisco.com/site/us/en/learn/training-certifications/certifications/devnet/associate/index.html" tooltiptext="Cisco DevNet Associate
    $300 Exam" target="_blank">DevNet A</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.comptia.org/certifications/cybersecurity-analyst" tooltiptext="CompTIA Cybersecurity Analyst+
    $404 exam" tabindex="0" target="_blank" >CySA+</a>
                    <a class="blueopsitem1" href="https://cybersecurity.isaca.org/csx-certifications/csx-practitioner-certification" tooltiptext="ISACA Cybersecurity Practitioner
    $549 lab" tabindex="0" target="_blank" >CSX-P</a>
                    <a class="blueopsitem1" href="https://www.mile2.com/network-forensics-examiner-outline/" tooltiptext="Mile2 Certified Network Forensics Examiner
    $550 exam
    Groups only" tabindex="0" target="_blank" >C)NFE</a>
                    <a class="blueopsitem1" href="https://www.giac.org/certification/open-source-intelligence-gosi" tooltiptext="GIAC Open Source Intelligence
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GOSI</a>
                    <a class="blueopsitem1" href="https://www.mile2.com/threat-analyst/" tooltiptext="Mile2 Certified Threat Intelligence Analyst
    $550 exam" tabindex="0" target="_blank" >C)TIA</a>
                    <a class="blueopsitem2" href="https://www.offensive-security.com/soc200-osda/" tooltiptext="Offensive Security Defense Analyst
    $2,499 exam
    Learning subscription required" tabindex="0" target="_blank" >OSDA</a>
                    <a class="redopsitem1" href="https://security.ine.com/certifications/emapt-certification/" tooltiptext="eLearnSecurity Mobile Application Penetration Tester
    $400" tabindex="0" target="_blank" >eMAPT</a>
                    <a class="redopsitem1" href="https://portswigger.net/web-security/certification" tooltiptext="Portswigger Burp Suite Certified Practioner
    $99 exam" target="_blank">BSCP</a>
                    <a class="redopsitem1" href="https://www.isecom.org/certification.html" tooltiptext="ISECOM OSSTMM Professional Security Tester
    Unknown" tabindex="0" target="_blank" >OPST</a>
                    <a class="redopsitem1" href="https://www.offensive-security.com/web200-oswa/" tooltiptext="Offensive Security Web Assessor
    $2,499 Exam
    Learning subscription required" tabindex="0" target="_blank" >OSWA</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://app.infosecinstitute.com/portal/courses/a0tC0000000Fp4IIAS" tooltipright="Infosec Institute Certified Reverse Engineering Analyst
    $4,599 exam
    Course required" tabindex="0" target="_blank" >CREA</a>
                    <!-- Row 20 -->
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.cwnp.com/certifications/cwsp" tooltipleft="CWNP Certified Wireless Security Professional
    $325 exam" tabindex="0" target="_blank" >CWSP</a>
                    <a class="networkitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-network-intrusion-analyst" tooltiptext="CREST Certified Network Intrusion Analyst
    $2,481 exam &amp; essay
    Hands on exam in UK" tabindex="0" target="_blank">CREST CCNIA</a>
                    <div class="spacer"></div>
                     <a class="iamitem1" href="https://www.identitymanagementinstitute.org/cige/" tooltiptext="IMI Certified Identity Governance Expert
    $395 exam" target="_blank">CIGE</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://docs.microsoft.com/en-us/learn/certifications/azure-administrator?wt.mc_id=learningredirect_certs-web-wwl" tooltiptext="Microsoft Azure Administrator Associate
    $165 exam" tabindex="0" target="_blank">AZ-104</a>
                    <a class="engineeritem1" href="https://pecb.com/en/education-and-certification-for-individuals/cloud-security/lead-cloud-security-manager" tooltiptext="PECB Lead Cloud Security Manager
    ~$930 exam
    Course required" tabindex="0" target="_blank" >CLCSM</a>
    <a class="engineeritem1" href="https://cert.eccouncil.org/certified-cloud-security-engineer.html" tooltiptext="EC Council Certified Cloud Security Engineer
    $100 exam
    EC Council Course Recommended" tabindex="0" target="_blank" >CCSE</a>
                    <a class="engineeritem1" href="https://www.mosse-institute.com/certifications/mcse-certified-cloud-security-engineer.html" tooltiptext="Mosse Institute Cloud Security Engineer
                    $600 exam" tabindex="0" target="_blank" >MCSE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" style="font-size:0.5vmax;" href="https://trailhead.salesforce.com/credentials/systemarchitect" tooltiptext="SalesForce System Architect
    $400 hands-on lab" tabindex="0" target="_blank" >SFSA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="assetitem2" href="https://www.asisonline.org/certification/associate-protection-professional-app/" tooltiptext="ASIS Associate Protection Professional
    $350 exam" tabindex="0" target="_blank" >ASIS APP</a>
                    <a class="mgmtitem1" href="https://www.eccouncil.org/programs/certified-network-defense-architect-cnda/" tooltiptext="EC Council Certified Network Defense Architect
    $200 application
    Requires CEH cert" tabindex="0" target="_blank" >CNDA</a>
                    <a class="mgmtitem1" href="https://drii.org/certification/acrp" tooltiptext="DRI Associate Cyber Resilience Professional
    $200 exam
    Course req" target="_blank">DACRP</a>
                    <a class="mgmtitem1" href="https://www.itgovernance.co.uk/shop/product/iso-27005-certified-isms-risk-management" tooltiptext="IBITGQ Certified ISO 27005 Information Security Management Specialist Risk Management
    $2,783 course exam
    Branded course required" tabindex="0" target="_blank" >CISRM</a>
                    <a class="mgmtitem1" href="https://drii.org/certification/crmp" tooltiptext="DRI Certified Risk Management Professional
    $400 exam
    Application essay" tabindex="0" target="_blank" >DCRMP</a>
                    <a class="mgmtitem1" href="https://www.sans.org/security-awareness-training/career-development/credential/" tooltiptext="SANS Security Awareness Professional
    $1219 Exam
    SANS MGT433 course recommended" tabindex="0" target="_blank" rel="noopener">SSAP</a>
                    <a class="mgmtitem1" href="https://www.oceg.org/certifications/grc-professional-certification/" tooltiptext="OCEG Governance, Risk, and Compliance Professional
    $399 12 month license" tabindex="0" target="_blank" rel="noopener">GRCP</a>
                    <a class="mgmtitem1" href="https://www.thehlayer.com/about-exam/" tooltiptext="The H Layer Security Awareness and Culture Professional
    $369 Exam" tabindex="0" target="_blank" rel="noopener">SACP</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/information_systems_security/cisp" tooltiptext="GAQM Certified Information Security Professional
    $170 exam" tabindex="0" target="_blank" >CISP</a>
                    <div class="spacer"></div>
                    <a class="testitem1" href="https://www.certipedia.com/quality_marks/0000063484?locale=en" tooltiptext="TUV Rheinland IT Security Auditor (GERMAN)
    $415 exam
    Course required" tabindex="0" target="_blank" >TUV Auditor</a>
                    <a class="testitem1" href="https://sharedassessments.org/ctprp/" tooltiptext="Shared Assessment Certified Third-Party Risk Professional
    $1295 course" target="_blank">CTPRP</a>                
                    <a class="testitem1" href="https://na.theiia.org/certification/CIA-Certification/Pages/CIA-Certification.aspx" tooltiptext="The Institute of Internal Auditors Certified Internal Auditor
    $1315 3 exams" target="_blank">IIA CIA</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://certnexus.com/certification/cyber-secure-coder/" tooltiptext="CertNexus Cyber Secure Coder
    $300 exam" tabindex="0" target="_blank" >CCSC</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://docs.microsoft.com/en-us/learn/certifications/security-operations-analyst/" tooltiptext="Microsoft Certified: Security Operations Analyst Associate
    ~$165 exam" tabindex="0" target="_blank">SC-200</a>
		            <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mrci-remote-cybersecurity-internship.html" tooltiptext="Mosse Institute Remote Cybersecurity Internship Programme
  $49 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MRCI</a>
		            <a class="blueopsitem1" href="https://www.eccouncil.org/programs/disaster-recovery-professional-edrp/" tooltiptext="EC Council Disaster Recovery Professional
    $450 exam" tabindex="0" target="_blank" >EDRP</a>
                    <a class="blueopsitem1" href="https://academy.hackthebox.com/preview/certifications/htb-certified-defensive-security-analyst" tooltiptext="Hack the Box Certified Defensive Security Analyst
                    $145 modules + $210 exam
                    $490 Subscription available" tabindex="0" target="_blank" >HTB CDSA</a>
                    <a class="blueopsitem1" href="https://certnexus.com/certification/cybersec-first-responder/" tooltiptext="CertNexus CyberSec First Responder
    $250 exam" tabindex="0" target="_blank" >CFR</a>
                    <a class="blueopsitem1" href="https://www.eccouncil.org/programs/certified-threat-intelligence-analyst-ctia/" tooltiptext="EC Council Certified Threat intelligence Analyst
    $450 exam" tabindex="0" target="_blank" >CTIA</a>
                    <a class="redopsitem1" href="https://thecyberscheme.org/cyber-scheme-team-member-cstm-exam/" tooltiptext="Cyber Scheme Team Member
    $610 exam" tabindex="0" target="_blank" >CSTM</a>
                    <a class="redopsitem1" href="https://ine.com/learning/certifications/internal/elearnsecurity-junior-penetration-tester-v2" tooltiptext="eLearnSecurity Junior Penetration Tester
    $249 lab" tabindex="0" target="_blank" >eJPT</a>
                    <a class="redopsitem1" href="hhttps://www.seco-institute.org/certifications/ethical-hacking-track/practitioner/" tooltiptext="SECO Ethical Hacking Practitioner
    $550 exam" tabindex="0" target="_blank" >S-EHP</a>
                    <a class="redopsitem1" href="https://www.isecom.org/certification.html" tooltiptext="ISECOM Certified Hacker Analyst Trainer
    $100 annual sub
    Unknown exam price" tabindex="0" target="_blank" >CHAT</a>
                    <a class="redopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-practitioner-security-analyst" tooltiptext="CREST Practitioner Security Analyst
    $425 exam" tabindex="0" target="_blank" >CREST CPSA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 21 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://view.ceros.com/f5/certification-roadmap/p/9?heightOverride=740" tooltipleft="F5 Big-IP Certified Administrator
    $135 exam" tabindex="0" target="_blank" >F5 CA</a>
                    <a class="networkitem1" href="https://www.elearnsecurity.com/certification/endp/" tooltipleft="eLearnSecurity Network Defense Professional
    $400 exam" tabindex="0" target="_blank" >eNDP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://www.identitymanagementinstitute.org/cist/" tooltiptext="IMI Certfied Identity and Security Technologist
    $295 exam" target="_blank">CIST</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://cloud.google.com/certification/cloud-security-engineer" tooltiptext="Google Professional Cloud Security Engineer
    $200 exam" tabindex="0" target="_blank" >Google PCSE</a>
                    <a class="engineeritem1" href="https://www.exin.com/certifications/ccc-professional-cloud-security-manager-exam" tooltiptext="EXIN Professional Cloud Security Manager
    $315 exam" tabindex="0" target="_blank" >EXIN PCSM</a>
                    <a class="engineeritem1" href="https://www.mosse-institute.com/certifications/mdso-certified-devsecops-engineer.html" tooltiptext="Mosse Institute Certified DevSecOps Engineer
    $450 exam" tabindex="0" target="_blank" >MDSO</a>
                    <a class="engineeritem1" href=" https://www.suse.com/training/exam/sca-sles-15/" tooltiptext="SUSE Certified Administrator
    $149 exam" tabindex="0" target="_blank" >SCA</a>
                    <a class="engineeritem1" href="https://www.isa.org/training-and-certifications/isa-certification/isa99iec-62443/isa99iec-62443-cybersecurity-certificate-programs/" tooltiptext="ISA Certified Automation Specialist
    $467 exam" tabindex="0" target="_blank" >ISA CAP</a>
                     <a class="engineeritem1" href="https://limessecurity.com/en/academy/ics-211/" tooltiptext="TUV Certified OT Security Manager
    $3,070 Course" tabindex="0" target="_blank" >TUV COSM</a>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.zachman.com/certification/what-we-certify/enterprise-architect" tooltiptext="Zachman Enterprise Architect Associate (Level 1)
    $2,999 course exam
    Branded course required" tabindex="0" target="_blank" >Zach EAA</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/scrum_agile/cad" tooltiptext="GAQM Certified Agile Developer
    $128 exam" tabindex="0" target="_blank">CAD</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/scrum_agile/cac" tooltiptext="GAQM Certified Agile Coach
    $170" tabindex="0" target="_blank">CAC</a>
                    <a class="mgmtitem1" href="https://www.ismi.org.uk/csmp/csmp%C2%AE-overview.aspx" tooltiptext="ISMI Certified Security Management Professional
    $1159" tabindex="0" target="_blank" >ISMI CSMP</a>
                    <a class="mgmtitem1" href="https://ecfirst.biz/index.php?route=product/product&path=59_61&product_id=89" tooltiptext="EC First Certified Security Compliance Specialist
    $695 exam" tabindex="0" target="_blank" >CSCS</a>
                    <a class="mgmtitem1" href="https://apmg-international.com/product/isoiec-27001" tooltiptext="APMG ISO/IEC 27001 Foundation
    $400 exam
    Application essay" tabindex="0" target="_blank" >APMG 27001F</a>
                    <a class="mgmtitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27001/iso-iec-27001-foundation" tooltiptext="PECB ISO/IEC 27001 Foundation
    $500-749 exam
    Course required" tabindex="0" target="_blank" >PECB 27001F</a>
                    <a class="mgmtitem1" href="https://www.mile2.com/cslo_outline/" tooltiptext="Mile2 Certified Security Leadership Officer
    $550 exam" tabindex="0" target="_blank" >C)SLO</a>
                    <a class="testitem2" href="https://drii.org/certification/cbca" tooltiptext="DRI Certified Business Continuity Auditor
    $400 exam
    Application req" target="_blank">DCBCA</a>
                    <a class="testitem1" href="https://www.oceg.org/certifications/grc-audit-certification/" tooltiptext="OCEG Governance, Risk, and Compliance Auditor
    $399 12 month license" tabindex="0" target="_blank" rel="noopener">GRCA</a>
                    <a class="testitem1" href="https://gaqm.org/certifications/information_systems_security/cisst" tooltiptext="GAQM Certified Information systems Security Tester
    $170 exam" tabindex="0" target="_blank" >CISST</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://www.mile2.com/cswae_outline/" tooltiptext="Mile2 Secure Web Application Engineer
    $550 exam" tabindex="0" target="_blank" >C)SWAE</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.isecom.org/certification.html" tooltiptext="ISECOM OSSTMM Professional Security Analyst
    $100 annual sub
    Unknown exam fee" tabindex="0" target="_blank" >OPSA</a>
                    <a class="blueopsitem1" href="https://cyberstruggle.org/aegis-certification/" tooltiptext="Cyber Struggle AEGIS
    $1,700 course exam
    Branded course required" tabindex="0" target="_blank" >CSAE</a>
                    <a class="blueopsitem1" href="https://www.asisonline.org/certification/professional-certified-investigator-pci" tooltiptext="ASIS Professional Certified Investigator
    $485 exam" tabindex="0" target="_blank" >ASIS PCI</a>
                    <a class="blueopsitem1" href="https://mitre-engenuity.org/mad/" tooltiptext="Mitre Att&ck Defender Security Operations Center Assessment
                    $299 annual subscription" tabindex="0" target="_blank" >MAD SOCA</a>
                    <a class="blueopsitem1" href="https://mitre-engenuity.org/mad/" tooltiptext="Mitre Att&ck Defender Cyber Threat intelligence
                    $299 annual subscription" tabindex="0" target="_blank" >MAD CTI</a>
                    <a class="redopsitem2" href="https://www.eccouncil.org/programs/certified-ethical-hacker-ceh/" tooltiptext="EC Council Certified Ethical Hacker
    $1,199 exam" tabindex="0" target="_blank" >CEH</a>
                    <a class="redopsitem1" href="https://secops.group/product/certified-appsec-pentester/" tooltiptext="The SecOps Group Certified AppSec Pentester
    $500 exam" tabindex="0" target="_blank" >SOG CAPen</a>
                    <a class="redopsitem1" href="https://www.mile2.com/penetration-testing-engineer-outline/" tooltiptext="Mile2 Certified Penetration Testing Engineer
    $550 exam" tabindex="0" target="_blank" >C)PTE</a>
                    <a class="redopsitem1" href="https://secops.group/product/certified-network-pentester/" tooltiptext="The SecOps Group Certified Network Pentester
    $500 exam" tabindex="0" target="_blank" >SOG CNPen</a>
                    <a class="redopsitem1" href="https://0xdarkvortex.dev/training-programs/red-team-and-operational-security/" tooltiptext="Dark Vortex Red Team & Operational Security
    $2500 exam
    Course required" tabindex="0" target="_blank" >DV RTOS</a>
                    <a class="redopsitem1" href="https://0xdarkvortex.dev/training-programs/offensive-tool-development/" tooltiptext="Dark Vortex Offensive Tool Development
    $2000 exam
    Course required" tabindex="0" target="_blank" >DV OTD</a>
                    <a class="redopsitem1" href="https://www.mosse-institute.com/certifications/mvre-vulnerability-researcher-and-exploitation-specialist.html" tooltipright="Mosse Institute Vulnerability Researcher and Exploitation Specialist
                    $450 Exam" tabindex="0" target="_blank" >MVRE</a>
                    <!-- Row 22 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.mosse-institute.com/certifications/mnse-network-security-essentials.html" tooltipleft="Mosse Institute Network Security Essentials
  $450 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MNSE</a>
                    <a class="networkitem1" href="https://www.paloaltonetworks.com/services/education/certification" tooltipleft="Palo Alto Networks Certified Network Security Administrator
  $155 exam" tabindex="0" target="_blank" >PCNSA</a>
                    <a class="networkitem1" href="https://www.isecom.org/certification.html" tooltiptext="ISECOM OSSTMM Wireless Security Expert
    $100 annual sub
    Unknown exam cost" tabindex="0" target="_blank" >OWSE</a>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://docs.microsoft.com/en-us/learn/certifications/identity-and-access-administrator/" tooltiptext="Microsoft Certfied: Identity and Access Administrator Associate
    $165 exam" target="_blank">SC-300</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://cloudsecurityalliance.org/education/ccsk/" tooltiptext="Cloud Security Alliance Certificate of Cloud Security Knowledge
    $395 exam" tabindex="0" target="_blank" >CSA CCSK</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://mile2.com/ccso_outline/" tooltiptext="Mile2 Certified Cloud Security Officer
    $550 exam" tabindex="0" target="_blank" >C)CSO</a>
                     <a class="engineeritem1" href="https://training.mirantis.com/dca-certification-exam/" tooltiptext="Docker Certified Associate
    $195 exam" tabindex="0" target="_blank" >DCA</a>
                    <a class="engineeritem1" href="https://www.lpi.org/our-certifications/lpic-1-overview" tooltiptext="Linux Professional Institute Certified: Linux Administrator
    $400 2 exams" tabindex="0" target="_blank" >LPIC-1</a>
                    <a class="engineeritem1" href="https://www.giac.org/certification/global-industrial-cyber-security-professional-gicsp" tooltiptext="GIAC Global Industrial Security Professional
    $979 exam
    SANS course encouraged" tabindex="0" target="_blank" >GICSP</a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem4x" href="https://www.giac.org/certification/security-essentials-gsec" tooltiptext="GIAC Security Essentials Certification
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" ><b>GSEC</b></a>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
		    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mois-certified-osint-expert.html" tooltiptext="MOIS Certified OSINT Expert Certification
  $450 certification programme
  100% practical. No expiry." tabindex="0" target="_blank">MOIS</a>
                    <a class="blueopsitem1" href="https://gaqm.org/certifications/information_systems_security/cfa" tooltiptext="GAQM Certified Forensic Analyst
    $128 exam" tabindex="0" target="_blank" >CFA</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.eccouncil.org/programs/certified-soc-analyst-csa/" tooltiptext="EC Council Certified SOC Analyst
    $550 exam" tabindex="0" target="_blank" >CSA</a>
                    <a class="blueopsitem2" href="https://www.giac.org/certifications/foundational-cybersecurity-technologies-gfact/" tooltiptext="GIAC Foundational Cybersecurity Technologies
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GFACT</a>
                    <a class="redopsitem1" href="https://secops.group/product/certified-mobile-pentester-cmpen-android/" tooltiptext="The SecOps Group Certified Mobile Pentester - Android
    $400 exam" tabindex="0" target="_blank" >SOG CMPen And</a>
                    <a class="redopsitem1" href="https://secops.group/product/certified-mobile-pentester-cmpen-ios/" tooltiptext="The SecOps Group Certified Mobile Pentester - iOS
    $400 exam" tabindex="0" target="_blank" >SOG CMPen iOS</a>
                    <a class="redopsitem1" href="https://0xdarkvortex.dev/training-programs/malware-on-steroids/#certification" tooltiptext="Dark Vortex Malware on Steroids
    $2000 exam
    Course required" tabindex="0" target="_blank" >DV MoS</a>
                    <a class="redopsitem1" style="font-size:0.5vmax;" href="https://www.comptia.org/certifications/pentest" tooltiptext="CompTIA Pentest+
    $404 exam" tabindex="0" target="_blank" >Pentest+</a>
                    <a class="redopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-certified-simulated-attack-specialist" tooltipright="CREST Certified Simulated Attack Specialist
    $2,520 2 exams &amp; lab" tabindex="0" target="_blank" >CREST CSAS</a>
                    <a class="redopsitem1" href="https://www.eccouncil.org/programs/ec-council-certified-encryption-specialist-eces/" tooltipright="EC Council Certified Encryption Specialist
    $249 exam" tabindex="0" target="_blank" >ECES</a>
                    <!-- Row 23 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://www.juniper.net/us/en/training/certification/certification-tracks/junos-security-track/?tab=jnciasec" tooltipleft="Juniper Networks Certified Internet Associate, Security
    $200 exam" tabindex="0" target="_blank" >JNCIA Sec</a>
                    <a class="networkitem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fca_cybersecurity" tooltipleft="Fortinet Certificed Associate
    Free course and exam required" tabindex="0" target="_blank" >FCA</a>
                    <a class="networkitem1" href="https://www.wcnacertification.com/exam-information-1" tooltipleft="Protocol Analysis Institute Wireshark Certified Network Analyst
    $299 exam" tabindex="0" target="_blank" >WCNA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.comptia.org/certifications/server" tooltiptext="CompTIA Server+
    $319 exam" tabindex="0" target="_blank" >Server+</a>
                    <a class="engineeritem1" href="https://www.practical-devsecops.com/certified-devsecops-professional/" tooltiptext="PDSO Certified DevSecOps Professional
    $799
    Exam and training bundled" tabindex="0" target="_blank" >PDSO CDP</a>
                    <a class="engineeritem1" href="https://www.exin.com/certifications/ccc-professional-cloud-developer-exam" tooltiptext="EXIN Professional Cloud Developer
    $315 exam" tabindex="0" target="_blank" >EXIN PCD</a>
    <a class="engineeritem1" href="https://www.cncf.io/certification/kcna/" tooltiptext="Cloud Native Computing Foundation Kubernetes and Cloud Native Associate
    $250 exam
    Branded course required" tabindex="0" target="_blank" >KCNA</a>
                    <a class="engineeritem1" href="https://www.comptia.org/certifications/linux" tooltiptext="CompTIA Linux+
    $369 exam" tabindex="0" target="_blank" >Linux+</a>
                    <a class="engineeritem1" href="https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty?wt.mc_id=learningredirect_certs-web-wwl" tooltiptext="Azure IoT Developer Specialty
    $165 exam" tabindex="0" target="_blank" >AZ-220</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://www.identitymanagementinstitute.org/crfs/" tooltiptext="IMI Certified Red Flag Specialist
    $295 exam" target="_blank">CRFS</a>
                    <div class="spacer5"></div>
                    <a class="mgmtitem4x" href="https://www.isc2.org/Certifications/SSCP" tooltiptext="(ISC)2 Systems Security Certified Practitioner
    $249 exam" tabindex="0" target="_blank" ><b>SSCP</b></a>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://secops.group/product/certified-application-security-practitioner/" tooltiptext="SecOps Group Certified AppSec Practitioner
    $249 exam" tabindex="0" target="_blank" >SOG CAP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.isaca.org/credentialing/ccoa" tooltiptext="ISACA Certified Cybersecurity Operations Analyst
    $760 exam" tabindex="0" target="_blank" >CCOA</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-practitioner-intrusion-analyst" tooltiptext="CREST Practitioner Intrusion Analyst
    $425 exam" tabindex="0" target="_blank" >CREST CPIA</a>
                    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mese-certified-enterprise-security-engineer.html" tooltiptext="Mosse Institute Enterprise Security Engineer
    $450 exam" tabindex="0" target="_blank" >MESE</a>
                    <a class="blueopsitem1" href="https://www.crest-approved.org/certification-careers/crest-certifications/crest-practitioner-threat-intelligence-analyst/" tooltiptext="CREST Practitioner Threat Intelligence Analyst
    $425 exam" tabindex="0" target="_blank" >CREST CPTIA</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.mosse-institute.com/certifications/mcpt-cloud-penetration-tester.html" tooltiptext="Mosse Institute Cloud Penetration Tester
    $450 exam" tabindex="0" target="_blank" >MCPT</a>
                    <a class="redopsitem1" href="https://mile2.com/professional-ethical-hacker/" tooltiptext="Mile2 Certified Professional Ethical Hacker
    $550 exam" tabindex="0" target="_blank" >C)PEH</a>
                    <a class="redopsitem1" href="https://gaqm.org/certifications/information_systems_security/cpeh" tooltiptext="GAQM Certified Professional Ethical Hacker
    $170 exam" tabindex="0" target="_blank" >GCPEH</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 24 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://training-certifications.checkpoint.com/#/courses/Check%20Point%20Certified%20Admin%20(CCSA)%20R80.x" tooltipleft="Checkpoint Certified Security Administrator
    $250 exam" tabindex="0" target="_blank" >CCSA</a>
                    <a class="networkitem1" href="https://certiport.filecamp.com/s/ITS_OD_102_Network_Security/fi" tooltipleft="Certiport IT Specialist - Network Security
    $127 exam" tabindex="0" target="_blank" >ITS-NS</a>
                    <a class="networkitem1" href="https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/entry/technician-cct.html" tooltiptext="Cisco Certified Technician
    $165 exam" tabindex="0" target="_blank" >CCT</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.comptia.org/certifications/cloud" tooltiptext="CompTIA Cloud+ 
    $369 exam" tabindex="0" target="_blank" >Cloud+</a>
                    <a class="engineeritem1" href="https://cloud.google.com/certification/cloud-engineer" tooltiptext="Google Associate Cloud Engineer
    $125 exam" tabindex="0" target="_blank" >Google ACE</a>
                    <a class="engineeritem1" href="https://secops.group/product/certified-cloud-security-practitioner-aws-ccsp-aws/" tooltiptext="SecOps Group Certified Cloud Security Practitioner - AWS
    $249 exam" tabindex="0" target="_blank" >SOG CCSP-AWS</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://training.linuxfoundation.org/certification/certified-it-associate/" tooltiptext="Linux Foundation Certified IT Associate
    $200 exam" tabindex="0" target="_blank" >LFCA</a>
                    <a class="engineeritem1" href="https://www.isa.org/training-and-certifications/isa-certification/isa99iec-62443/isa99iec-62443-cybersecurity-certificate-programs/" tooltiptext="ISA Certified Fundamentals Specialist
    $2,700 course + exam
    Course required" tabindex="0" target="_blank" >ISA CFS</a>
                    <a class="engineeritem1" style="font-size:0.5vmax;" href="https://eitca.org/eitca-is-information-security-academy/" tooltiptext="EITCA/IS Information Security Certificate
    $120 exam" tabindex="0" target="_blank" >EITCA/IS</a>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://iapp.org/certify/cipp" tooltiptext="IAPP Certified Information Privacy Professional
    $550 exam" tabindex="0" target="_blank" >CIPP</a>
                    <div class="spacer5"></div>
                    <a class="mgmtitem4x" href="https://www.comptia.org/certifications/security" tooltiptext="CompTIA Security+
    $404 exam" tabindex="0" target="_blank" ><b>Security+</b></a>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <a class="blueopsitem1" href="https://www.eccouncil.org/programs/certified-security-specialist-ecss/" tooltiptext="EC Council Certified Security Specialist
    $249 exam" tabindex="0" target="_blank" >ECSS</a>
                    <a class="blueopsitem1" href="https://www.mile2.com/cdfe_outline/" tooltiptext="Mile2 Certified Digital Forensics Examiner
    $550 exam" tabindex="0" target="_blank" >C)DFE</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.seco-institute.org/get-trained/cyber-defense-track/associate-soc-analyst-certification/" tooltiptext="SECO Associate SOC Analyst
    $480 exam" tabindex="0" target="_blank" >S-SA</a>
                    <a class="blueopsitem1" href="https://0xdarkvortex.dev/training-programs/adversary-operations-and-proactive-hunting/" tooltiptext="Dark Vortex Adversary Operations and Proactive Hunting
    $2500 exam
    Course required" tabindex="0" target="_blank" >DV AOPH</a>
                    <div class="spacer"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
                    <!-- Row 25 -->
                    <div class="skilllevelitem"><span style="color:var(--greendk)">Beginner</span></div>
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://secops.group/product/certified-network-security-practitioner/" tooltiptext="SecOps Group Certified Network Security Practitioner
    $249 exam" tabindex="0" target="_blank" >SOG NSP</a>
                    <a class="networkitem1" href="https://www.comptia.org/certifications/network" tooltiptext="CompTIA Network+
    $369 exam" tabindex="0" target="_blank" >Net+</a>
                    <div class="spacer"></div>
                    <a class="iamitem1" href="https://www.identitymanagementinstitute.org/cams/" tooltiptext="IMI Certfied Access Management Specialist
    $195 exam" tabindex="0" target="_blank" >CAMS</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://docs.microsoft.com/en-us/learn/certifications/azure-fundamentals" tooltiptext="Microsoft Azure Fundamentals
    $165 exam" tabindex="0" target="_blank" >AZ-900</a>
                    <a class="engineeritem1" href="https://www.mosse-institute.com/certifications/mcsf-cloud-services-fundamentals.html" tooltiptext="Mosse Institute Cloud Services Fundamentals
                    $450 exam" tabindex="0" target="_blank" >MCSF</a>
                    <a class="engineeritem1" href="https://www.mosse-institute.com/certifications/msaf-system-administration-fundamentals.html" tooltiptext="Mosse Institute System Administration Fundamentals
                    $450 exam" tabindex="0" target="_blank" >MSAF</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://training.apple.com/us/en/recognition" tooltiptext="Apple Certified Support Professional
    $250 exam
    Limited test locations" tabindex="0" target="_blank" >Apple ACSP</a>
                    <a class="engineeritem1" href="https://www.exidacace.com/Apply/CACS" tooltiptext="Excida IEC 62443 Certified Automation Cybersecurity Specialist
    $700 exam" tabindex="0" target="_blank" >CACS</a>
                    <a class="engineeritem1" href="https://limessecurity.com/en/academy/ics-211/" tooltiptext="TUV Certified OT Security Technical Expert
    $3,070 course" tabindex="0" target="_blank" >TUV COSTE</a>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://www.exin.com/certifications/exin-privacy-and-data-protection-foundation-exam" tooltiptext="EXIN Privacy and Data Protection Foundation
    $207 exam" tabindex="0" target="_blank" >EPDPF</a>
                    <a class="mgmtitem2" href="https://www.opengroup.org/certifications/togaf" tooltiptext="OpenGroup TOGAF Certified
    $360 exam" tabindex="0" target="_blank" >TOGAF Fdn</a>
                    <a class="mgmtitem1" href="https://gaqm.org/certifications/scrum_agile/csp-410" tooltiptext="GAQM Certified SAFe Practitioner
    $170 exam" tabindex="0" target="_blank" >CSP</a>
                    <a class="mgmtitem1" href="https://www.iiba.org/certification/iiba-certifications/specialized-business-analysis-certifications/certificate-in-cybersecurity-analysis/" tooltiptext="IIBA Certification in Cybersecurity Analysis
    $475 exam" tabindex="0" target="_blank" >IIBA CCA</a>
                    <a class="mgmtitem1" href="https://www.itgovernance.co.uk/shop/product/implementing-it-governance-foundation-principles-training-course" tooltiptext="IBITGQ Certified in Implementing IT Governance - Foundation &amp; Principles
    ~$2,499 course exam
    Branded course required" tabindex="0" target="_blank" >CITGP</a>
                    <a class="mgmtitem1" href="https://www.mile2.com/iscap_outline/" tooltiptext="Mile2 Information Systems Certification and Accredidation Professional
    $550 exam" tabindex="0" target="_blank" >C)ISCAP</a>
                    <a class="mgmtitem1" href="https://app.infosecinstitute.com/portal/courses/a0t0y000009lTzjAAE" tooltiptext="Infosec Institute Certified Security Awareness Practitioner
    $2,599 exam
    Course required" tabindex="0" target="_blank" >CSAP</a>
                    <a class="mgmtitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27032/iso-iec-27032-foundation" tooltiptext="PECB ISO/IEC 27032 Foundation
    $500-749 exam
    Course required" tabindex="0" target="_blank" >PECB 27032F</a>
                    <a class="mgmtitem1" href="https://www.mosse-institute.com/certifications/mcl-cybersecurity-leadership.html" tooltiptext="Mosse Institute Cybersecurity Leadership
                    $450 exam" tabindex="0" target="_blank" >MCL</a>
                    <a class="mgmtitem1" href="https://certiport.filecamp.com/s/JTIy1sX0ci0ZI3ss/fi" tooltiptext="Certiport IT Specialist - Cybersecurity
                    $127 exam" tabindex="0" target="_blank" >ITS-C</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="testitem1" href="https://www.exin.com/qualification-program/exin-cyber-and-it-security" tooltiptext="EXIN Cyber &amp; IT Security
    $225 exam" tabindex="0" target="_blank" >EXIN CIT</a>
                    <a class="testitem1" href="https://www.tuv.com/landingpage/en/training-functional-safety-cyber-security/detail-pages/zertifikate/cs-specialist.html" tooltiptext="TUV Rheinland Cybersecurity Specialist (GERMAN)
    $415 exam
    Course required" tabindex="0" target="_blank" >TUV CySec</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://gaqm.org/certifications/software_security_testing/csst" tooltiptext="GAQM Certified Software Security Tester
    $170 exam" tabindex="0" target="_blank" >CSST</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.isecom.org/certification.html" tooltiptext="ISECOM OSSTMM Professional Security Expert
    $100 annual sub
    Unknown exam cost" tabindex="0" target="_blank" >OPSE</a>
                    <a class="blueopsitem1" href="https://www.itgovernance.co.uk/shop/product/cyber-incident-response-management-foundation-training-course" tooltiptext="IBITGQ Cyber Incident Response Management Foundation
    $768 course exam
    Branded course required" tabindex="0" target="_blank" >CSX-F</a>
                    <div class="spacer"></div>
                     <a class="blueopsitem1" href="https://0xdarkvortex.dev/training-programs/malware-incident-and-log-forensics/" tooltiptext="Dark Vortex Malware Incident and Log Foensics
    $2000 exam" tabindex="0" target="_blank" >DV MILF</a>
                    <a class="blueopsitem1" href="https://www.itgovernance.co.uk/shop/product/cyber-incident-response-management-foundation-training-course" tooltiptext="IBITGQ Cyber Incident Response Management Foundation
    $768 course exam
    Branded course required" tabindex="0" target="_blank" >CIRM Fdn</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.exin.com/certifications/exin-ethical-hacking-foundation-exam" tooltiptext="EXIN Ethical Hacking Foundation
    $232 exam" tabindex="0" target="_blank" >EEHF</a>
                    <a class="redopsitem1" href="https://www.seco-institute.org/certifications/ethical-hacking-certification-track/ethical-hacking-foundation/" tooltiptext="SECO Ethical Hacking Foundation
    $460 exam" tabindex="0" target="_blank" >S-EHF</a>
                    <a class="redopsitem1" href="https://www.isecom.org/certification.html" tooltiptext="ISECOM Certified Hacker Analyst
    $100 annual sub
    Unknown exam cost" tabindex="0" target="_blank" >CHA</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 26 -->
                    <div class="spacer"></div>
                    <a class="networkitem1" href="https://training.fortinet.com/local/staticpage/view.php?page=fcf_cybersecurity" tooltipleft="Fortinet Certified Fundamentals Cybersecurity
    Free 3 courses with exams req" tabindex="0" target="_blank" >FCF</a>
                    <a class="networkitem1" href="https://www.paloaltonetworks.com/services/education/certification" tooltipleft="Palo Alto Networks Certified Cybersecurity Entry-level Technician
    $110 exam" tabindex="0" target="_blank" >PCCET</a>
	            <div class="spacer"></div>
		    <div class="spacer"></div>
		    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://aws.amazon.com/certification/certified-cloud-practitioner/" tooltiptext="Amazon Web Services Certified Cloud Practitioner
    $100 exam" tabindex="0" target="_blank" >AWS CP</a>
                    <a class="engineeritem1" href="https://www.exin.com/certifications/ccc-professional-cloud-administrator-exam" tooltiptext="EXIN Professional Cloud Administrator
    $315 exam" tabindex="0" target="_blank" >EXIN PCA</a>
                    <a class="engineeritem1" href="https://www.comptia.org/certifications/a" tooltiptext="CompTIA A+
    $253 exam" tabindex="0" target="_blank" >A+</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://certnexus.com/certification/ciotsp/" tooltiptext="CertNexus Certified Internet of Things Security Practitioner
    $250 exam" tabindex="0" target="_blank" >CIOTSP</a>
                    <a class="engineeritem1" href="https://limessecurity.com/en/academy/ics-201/" tooltiptext="TUV Certified OT Security Practitioner
    $2725 course" tabindex="0" target="_blank" >TUV COSP</a>
                    <div class="spacer"></div>
                    <a class="assetitem1" href="https://www.exin.com/certifications/exin-privacy-and-data-protection-essentials-exam" tooltiptext="EXIN Privacy and Data Protection Essentials
    $145 exam" tabindex="0" target="_blank" >EPDPE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.axelos.com/certifications/propath/mor-risk-management/mor-foundation" tooltiptext="Axelos M_o_R Framework Foundation
    $495 exam" tabindex="0" target="_blank" >M_o_R Fdn</a>
                    <a class="mgmtitem1" href="https://risklens-academy.myshopify.com/collections/popular-courses/products/fair-analysis-fundamentals-2" tooltiptext="Fair Institute Analysis Fundamentals
    $1499 exam
    Course required" tabindex="0" target="_blank" >Fair Fdn</a>
                    <a class="mgmtitem1" href="https://www.scrum.org/assessments/professional-scrum-master-i-certification" tooltiptext="Scrum.org Professional Scrum Master I
    $150 exam" tabindex="0" target="_blank" >PSM I</a>
                    <a class="mgmtitem1" href="https://apmg-international.com/product/iso-20000" tooltiptext="APMG ISO/IEC 20000 Foundation
    $308 exam" tabindex="0" target="_blank" >APMG 20000F</a>
                    <a class="mgmtitem1" href="https://www.ismi.org.uk/csmp/certified-security-manager%C2%AE" tooltiptext="ISMI Certified Security Manager
    $TBD" tabindex="0" target="_blank" >ISMI CSM</a>
                    <a class="mgmtitem1" href="https://www.bcs.org/get-qualified/certifications-for-professionals/information-security-and-ccp-scheme-certifications/bcs-foundation-certificate-in-information-security-management-principles/" tooltiptext="BCS Foundation Certifiate in Information Security Management Principles
    $249 exam" tabindex="0" target="_blank" >BCS FISMP</a>
                    <a class="mgmtitem1" href="https://www.isc2.org/Certifications/CC" tooltiptext="ISC2 Certified in Cybersecurity
    Free exam" tabindex="0" target="_blank" >CC</a>
                    <a class="mgmtitem1" href="https://www.seco-institute.org/certifications/information-security-certification-track/" tooltiptext="SECO Information Security Foundation
                    $460 exam" tabindex="0" target="_blank" >S-ISF</a>
                    <a class="mgmtitem2" href="https://www.giac.org/certification/information-security-fundamentals-gisf" tooltiptext="GIAC Information Security Fundamentals
    $979 exam
    SANS course recommended" tabindex="0" target="_blank" >GISF</a>
                    <div class="spacer"></div>
                    <a class="testitem1" style="font-size:0.5vmax;" href="https://www.is-its.org/seminare/isits-seminarangebot/cybersecurity-awareness-beauftragter" tooltiptext="TUV Rheinland Cybersecurity Awareness (GERMAN)
    $415 exam
    Course required" tabindex="0" target="_blank" >TUV CyAware</a>
                    <div class="spacer"></div>
                    <a class="softwareitem1" href="https://www.mosse-institute.com/certifications/mase-certified-application-security-engineer.html" tooltiptext="Mosse Institute Certified Application Security Engineer
    $450 exam" tabindex="0" target="_blank">MASE</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.mile2.com/csp_outline/" tooltiptext="Mile2 Certified Security Principles
    $550 exam" tabindex="0" target="_blank" >C)SP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.eccouncil.org/programs/certified-network-defender-cnd/" tooltiptext="EC Council Certified Network Defender
    $550 exam" tabindex="0" target="_blank" >CND</a>
                    <div class="spacer"></div>
                    <a class="redopsitem1" href="https://www.mile2.com/vulnerability-assessor-outline/" tooltiptext="Mile2 Certified Vulnerability Assessor
    $550 exam" tabindex="0" target="_blank" >C)VA</a>
                    <a class="redopsitem1" href="https://kali.training/klcp/" tooltiptext="Kali Linux Certified Professional
    $299 exam" tabindex="0" target="_blank" >KLCP</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <!-- Row 27 -->
                    <div class="spacer"></div>
                    <div class="spacer5"></div>
                    <a class="iamitem1" href="https://docs.microsoft.com/en-us/learn/certifications/security-compliance-and-identity-fundamentals/" tooltiptext="Microsoft Certified: Security, Compliance, and Identity Fundamentals
    $99 exam" tabindex="0" target="_blank" >SC-900</a>
                    <div class="spacer"></div>
                    <a class="engineeritem1" href="https://www.comptia.org/certifications/cloud-essentials" tooltiptext="CompTIA Cloud Essentials
    $138 exam" tabindex="0" target="_blank" >Cloud Essnt</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <a class="mgmtitem2" href="https://www.axelos.com/certifications/itil-certifications/itil-foundation" tooltiptext="ITIL Foundation
    $383 exam" tabindex="0" target="_blank" >ITIL Fdn</a>
                    <a class="mgmtitem1" href="https://www.comptia.org/certifications/project" tooltiptext="CompTIA Project+
    $369 exam" tabindex="0" target="_blank" >Project+</a>
                   <a class="mgmtitem1" href="https://www.ciisec.org/ICSF_Exam" tooltiptext="CIISec Information and Cybersecurity Fundamentals
    $450 exam" tabindex="0" target="_blank" >CIISec ICSF</a>
                    <div class="spacer"></div>
                    <a class="mgmtitem1" href="https://www.exin.com/certifications/information-security-foundation-based-iso-iec-27001-exam?language_content_entity=en" tooltiptext="EXIN Information Security Foundation
    $232 exam" tabindex="0" target="_blank" >FEXIN</a>
                    <a class="mgmtitem1" href="https://www.exin.com/certifications/information-security-foundation-based-iso-iec-27001-exam" tooltiptext="EXIN ISO/IEC 27001 Foundation
    $232 exam" tabindex="0" target="_blank" >EXIN 27001F</a>
                   <a class="mgmtitem1" href="https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27005/iso-iec-27005-foundation" tooltiptext="PECB ISO/IEC 27005 Foundation
    $500-749 exam
    Course required" tabindex="0" target="_blank" >PECB 27005F</a>
                    <a class="mgmtitem1" href="https://www.itgovernance.co.uk/shop/product/certified-cyber-security-foundation-training-course" tooltiptext="IBITGQ Certified Cyber Security Foundation
    $725 course exam
    Branded course required" tabindex="0" target="_blank" >C CS F</a>
                    <a class="mgmtitem1" href="https://www.itgovernance.co.uk/shop/product/certified-iso-27001-isms-foundation-training-course" tooltiptext="IBITGQ Certified ISO 27001 Information Security Management Specialist Foundation
    $853 course exam
    Brandeed course required" tabindex="0" target="_blank" >CIS F</a>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div>
                    <div class="spacer"></div><a class="softwareitem1" href="https://www.seco-institute.org/certifications/secure-software-certification-track/secure-programming-foundation/" tooltiptext="SECO Secure Programming Foundation
                    $460 exam" tabindex="0" target="_blank" >S-SPF</a>
                    <div class="spacer"></div>
                    <a class="blueopsitem1" href="https://www.eccouncil.org/Certification/certified-secure-computer-user" tooltiptext="EC Council Certified Secure Computer User
                    $125 exam" tabindex="0" target="_blank" >CSCU</a>
                    <a class="blueopsitem1" href="https://www.mosse-institute.com/certifications/mics-introduction-to-cyber-security.html" tooltiptext="Mosse Institute Introductions to Cyber Security
                    Free exam" tabindex="0" target="_blank" >MICS</a>
                    <div class="spacer5"></div>
                    <div class="spacer5"></div>
                    <div class="spacer"></div>
            </div>
            <!-- Find # of certs by searching for _bl@nk replacing the @ for a -->
            <div class="key">481 certifications listed | July 2024</div>
            <div class="key"> <br></div>
    </div># Roadmap
