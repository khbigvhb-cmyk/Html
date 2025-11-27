<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CEEII Facilities Network</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* ==================================== */
        /* I. THEME AND BASE STYLES */
        /* ==================================== */
        :root {
            --primary-blue: #004d99; /* CEEII/Tech Primary Color */
            --secondary-green: #38761d; /* Agro-Industry Accent Color */
            --light-bg: #f8f9fa;
            --border-color: #dee2e6;
        }

        body {
            font-family: 'Roboto', Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background-color: var(--light-bg);
            color: #333;
        }

        #ceii-facilities-tabbed {
            max-width: 1200px;
            margin: 0 auto;
            background-color: #fff;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05); /* Soft shadow effect */
        }

        h2 {
            color: var(--primary-blue);
            text-align: center;
            margin-bottom: 25px;
            font-weight: 700;
        }

        h3 {
            color: var(--secondary-green);
            border-bottom: 2px solid #e9ecef;
            padding-bottom: 5px;
            margin-top: 0;
        }
        
        /* ==================================== */
        /* II. TAB NAVIGATION STYLING */
        /* ==================================== */
      .tabs {
            display: flex;
            border-bottom: 3px solid var(--primary-blue); /* Strong separation line */
            margin-bottom: 20px;
            overflow-x: auto; /* Handle overflow on small screens */
        }

      .tab-button {
            padding: 12px 20px;
            cursor: pointer;
            border: none;
            background-color: var(--light-bg);
            border-top-left-radius: 8px;
            border-top-right-radius: 8px;
            transition: all 0.3s ease; /* Smooth transition effect */
            margin-right: 5px;
            font-weight: 500;
            color: #666;
            white-space: nowrap; /* Prevents wrapping */
        }

      .tab-button:hover {
            background-color: #e2e6e9; /* Hover effect */
            color: #000;
        }

      .tab-button.active {
            background-color: #fff;
            border: 1px solid var(--primary-blue);
            border-bottom: 3px solid #fff; /* Creates the "connected" effect */
            color: var(--primary-blue);
            font-weight: 700;
            box-shadow: 0 -2px 5px rgba(0, 0, 0, 0.05);
        }

        /* ==================================== */
        /* III. CONTENT PANEL STYLING */
        /* ==================================== */
      .tab-content {
            display: none; /* Hidden by default */
            padding: 25px;
            border: 1px solid var(--border-color);
            border-radius: 0 0 8px 8px;
            background-color: #fff;
        }

      .tab-content ul {
            padding-left: 20px;
        }

        /* Table Styling for Facility Lists */
      .tab-content table {
            width: 100%;
            border-collapse: separate; /* Allows border-radius on cells */
            border-spacing: 0;
            margin-top: 20px;
        }

      .tab-content th,.tab-content td {
            border: 1px solid var(--border-color);
            padding: 12px;
            text-align: left;
        }

      .tab-content th {
            background-color: #eaf0f6;
            color: var(--primary-blue);
            font-weight: 700;
        }
        
      .tab-content tr:nth-child(even) {
            background-color: #f7f7f7; /* Stripe effect for readability */
        }
      .tab-content tr:hover {
            background-color: #eef; /* Row hover effect */
        }

    </style>
</head>
<body>

    <section id="ceii-facilities-tabbed">
        <h2>CEEII Facilities: A Network for Agro-Industry Innovation</h2>
        <p>
            The Center of Excellence in Entrepreneurship, Innovation, and Invention (CEEII) operates on a Hub-and-Spoke model. Explore the resources available at each level of our network to find the tools you need for innovation, from virtual collaboration to advanced prototyping.
        </p>

        <div class="tabs">
            <button class="tab-button active" onclick="openTab(event, 'DigitalEcosystem')">I. Digital & Virtual Ecosystem</button>
            <button class="tab-button" onclick="openTab(event, 'UoRHub')">II. UoR Hub: Specialized Facilities</button>
            <button class="tab-button" onclick="openTab(event, 'SatelliteCenters')">III. Satellite Centers (UoP, RUSL, HCBT, NU, CMU)</button>
        </div>

        <div id="DigitalEcosystem" class="tab-content" style="display: block;">
            <h3>Digital & Virtual Ecosystem (Shared Resources)</h3>
            <p>This suite serves as the core of the CEEII, connecting all partner universities virtually and providing centralized platforms for project management, education, and industry linkage.</p>
            <ul>
                <li>
                    <strong>Project & Network Management:</strong> FOUNTAIN Project Management Portal and the central CEEII Website (Hosted on Ruhuna server).
                </li>
                <li>
                    <strong>Industry Collaboration (IPO Web):</strong> A customizable online package distributed to all partner universities to manage their Industry Placement Office (IPO) activities and facilitate industry linkages.
                </li>
                <li>
                    <strong>Global Outreach:</strong> Connection to the Global Agro-Industry FORUM (GAIF) and the Virtual Product Launch Space.
                </li>
                <li>
                    <strong>Educational Platforms:</strong> The Curriculum Development Management Portal and connection to Learning Resources (MOOCS) platforms.
                </li>
                <li>
                    <strong>Consultation Services:</strong> Virtual Consultation Service for Incubation embedded within the CEEII framework.
                </li>
            </ul>
        </div>

        <div id="UoRHub" class="tab-content">
            <h3>UoR Hub: Specialized Facilities (University of Ruhuna)</h3>
            <p>The UoR Hub is the central location for advanced capabilities, featuring a larger experimentation lab and a state-of-the-art media studio for complex prototyping, professional testing, and global outreach.</p>

            <table>
                <thead>
                    <tr>
                        <th>Facility / Lab</th>
                        <th>Primary Function / Focus</th>
                        <th>Key Equipment (UoR Exclusive)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>Product Launch Studio (AV Studio)</strong></td>
                        <td>High-fidelity media production, virtual product launches, and professional remote collaboration.</td>
                        <td>Integrated Video Conferencing System, Video Mixer (4 inputs), Chroma key screen, Drone, Processing Workstations, Zoom license.</td>
                    </tr>
                    <tr>
                        <td><strong>Mini Food Technology Lab</strong></td>
                        <td>Advanced product R&D, professional quality control, and food science analysis.</td>
                        <td><strong>Texture analyzer</strong> (for physical property testing), **Refractometers**, Freezer (400 l), Gas cooker (with oven), Impulse Pedal sealer.</td>
                    </tr>
                    <tr>
                        <td><strong>Mini Machinery Lab</strong></td>
                        <td>Complex mechanical prototyping, custom part fabrication, and light engineering.</td>
                        <td>**Bench Lathe** (precision machining), Metal Benders, Bench Drill, Welding Plant, Safety accessories.</td>
                    </tr>
                    <tr>
                        <td><strong>Mini Electronic Lab</strong></td>
                        <td>Advanced electronic diagnostics, circuit testing, and network infrastructure maintenance.</td>
                        <td>**Oscilloscope** (for signal testing), PoE & LAN cable tester, Fiber cable tester, Heavy Duty Heat Hot Air Gun.</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div id="SatelliteCenters" class="tab-content">
            <h3>Satellite Centers: Foundational Capacity</h3>
            <p>All Satellite Centers (UoP, RUSL, HCBT, NU, CMU) received an identical, standardized package of equipment to enable localized outreach, initial prototyping, basic experimentation, and robust digital connectivity.</p>

            <table>
                <thead>
                    <tr>
                        <th>Facility Category</th>
                        <th>Scope of Capacity</th>
                        <th>Key Standardized Equipment (Available at Each Center)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>UIC Platform & Mobility</strong></td>
                        <td>Administrative support, general IT access, local workshops, and presentations.</td>
                        <td>Laptop Computers, Multi-function Printers, Wi-Fi Access Points, Portable Sound Systems (battery powered).</td>
                    </tr>
                    <tr>
                        <td><strong>Foundational Prototyping</strong></td>
                        <td>Preliminary testing in food processing, basic electronics, and light fabrication/repair.</td>
                        <td>Gas cooker (4 burners), Food processer (750W), Benchtop sealer, SMD Station, Digital Multimeter, Electric Drill, Welding Plant, Tool Box.</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>

    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tabbuttons;

            // 1. Hide all tab content
            tabcontent = document.getElementsByClassName("tab-content");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }

            // 2. Deactivate all tab buttons
            tabbuttons = document.getElementsByClassName("tab-button");
            for (i = 0; i < tabbuttons.length; i++) {
                tabbuttons[i].className = tabbuttons[i].className.replace(" active", "");
            }

            // 3. Show the specific tab content and activate the button
            document.getElementById(tabName).style.display = "block";
            // Add ' active' class to the current button
            evt.currentTarget.className += " active";
        }
    </script>

</body>
</html># Html
