<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CEEII Facilities Network</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-blue: #004d99;
            --secondary-green: #38761d;
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
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
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
        
        .tabs {
            display: flex;
            border-bottom: 3px solid var(--primary-blue);
            margin-bottom: 20px;
            overflow-x: auto;
        }

        .tab-button {
            padding: 12px 20px;
            cursor: pointer;
            border: none;
            background-color: var(--light-bg);
            border-top-left-radius: 8px;
            border-top-right-radius: 8px;
            transition: all 0.3s ease;
            margin-right: 5px;
            font-weight: 500;
            color: #666;
            white-space: nowrap;
        }

        .tab-button:hover {
            background-color: #e2e6e9;
            color: #000;
        }

        .tab-button.active {
            background-color: #fff;
            border: 1px solid var(--primary-blue);
            border-bottom: 3px solid #fff;
            color: var(--primary-blue);
            font-weight: 700;
            box-shadow: 0 -2px 5px rgba(0, 0, 0, 0.05);
        }

        .tab-content {
            display: none;
            padding: 25px;
            border: 1px solid var(--border-color);
            border-radius: 0 0 8px 8px;
            background-color: #fff;
        }

        .tab-content ul {
            padding-left: 20px;
        }

        .tab-content table {
            width: 100%;
            border-collapse: separate;
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
            background-color: #f7f7f7;
        }
        .tab-content tr:hover {
            background-color: #eef;
        }

        /* Reservation modal styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1001;
            left: 0; top: 0;
            width: 100%; height: 100%;
            overflow: auto;
            background: rgba(0,0,0,0.4);
        }
        .modal-content {
            background-color: #fff;
            margin: 10vh auto;
            padding: 30px 24px 20px 24px;
            border: 1px solid var(--border-color);
            border-radius: 10px;
            max-width: 400px;
            box-shadow: 0 0 30px rgba(0,0,0,0.08);
        }
        .close-modal {
            color: #999;
            float: right;
            font-size: 24px;
            font-weight: bold;
            cursor: pointer;
        }
        .close-modal:hover {
            color: #d00;
        }
        #reservation-message {
            font-size: 16px;
            color: var(--secondary-green);
            margin-top: 15px;
        }
        label {
            font-weight: 500;
            display: block;
            margin-top: 16px;
            margin-bottom: 4px;
        }
        input, select, textarea {
            font-size: 15px;
            width: 100%;
            padding: 7px 8px;
            border-radius: 5px;
            border: 1px solid var(--border-color);
            box-sizing: border-box;
        }
        button[type="submit"] {
            background-color: var(--primary-blue);
            color: #fff;
            border: none;
            padding: 10px 24px;
            margin-top: 18px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            font-size: 15px;
            transition: background 0.2s;
        }
        button[type="submit"]:hover {
            background-color: #003662;
        }
        .reserve-link {
            display: inline-block;
            margin-left: 8px;
            background: var(--secondary-green);
            color: #fff!important;
            border-radius: 4px;
            font-size: 13px;
            padding: 2px 8px;
            cursor: pointer;
            text-decoration: none;
            transition: background 0.18s;
        }
        .reserve-link:hover {
            background: #225710;
            text-decoration: underline;
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
            <button class="tab-button active" onclick="openTab(event, 'DigitalEcosystem')">I. Digital &amp; Virtual Ecosystem</button>
            <button class="tab-button" onclick="openTab(event, 'UoRHub')">II. UoR Hub: Specialized Facilities</button>
            <button class="tab-button" onclick="openTab(event, 'SatelliteCenters')">III. Satellite Centers (UoP, RUSL, HCBT, NU, CMU)</button>
        </div>

        <div id="DigitalEcosystem" class="tab-content" style="display: block;">
            <h3>Digital &amp; Virtual Ecosystem (Shared Resources)</h3>
            <p>This suite serves as the core of the CEEII, connecting all partner universities virtually and providing centralized platforms for project management, education, and industry linkage.</p>
            <ul>
                <li>
                    <strong>Project &amp; Network Management:</strong> FOUNTAIN Project Management Portal and the central CEEII Website (Hosted on Ruhuna server).
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
                        <td>
                            <strong>Product Launch Studio (AV Studio)</strong>
                            <a href="#" class="reserve-link" onclick="openReservation('Product Launch Studio (AV Studio)');return false;">Reserve</a>
                        </td>
                        <td>High-fidelity media production, virtual product launches, and professional remote collaboration.</td>
                        <td>Integrated Video Conferencing System, Video Mixer (4 inputs), Chroma key screen, Drone, Processing Workstations, Zoom license.</td>
                    </tr>
                    <tr>
                        <td>
                            <strong>Mini Food Technology Lab</strong>
                            <a href="#" class="reserve-link" onclick="openReservation('Mini Food Technology Lab');return false;">Reserve</a>
                        </td>
                        <td>Advanced product R&amp;D, professional quality control, and food science analysis.</td>
                        <td><strong>Texture analyzer</strong> (for physical property testing), Refractometers, Freezer (400 l), Gas cooker (with oven), Impulse Pedal sealer.</td>
                    </tr>
                    <tr>
                        <td>
                            <strong>Mini Machinery Lab</strong>
                            <a href="#" class="reserve-link" onclick="openReservation('Mini Machinery Lab');return false;">Reserve</a>
                        </td>
                        <td>Complex mechanical prototyping, custom part fabrication, and light engineering.</td>
                        <td>Bench Lathe (precision machining), Metal Benders, Bench Drill, Welding Plant, Safety accessories.</td>
                    </tr>
                    <tr>
                        <td>
                            <strong>Mini Electronic Lab</strong>
                            <a href="#" class="reserve-link" onclick="openReservation('Mini Electronic Lab');return false;">Reserve</a>
                        </td>
                        <td>Advanced electronic diagnostics, circuit testing, and network infrastructure maintenance.</td>
                        <td>Oscilloscope (for signal testing), PoE &amp; LAN cable tester, Fiber cable tester, Heavy Duty Heat Hot Air Gun.</td>
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
                        <td>
                            <strong>UIC Platform &amp; Mobility</strong>
                            <a href="#" class="reserve-link" onclick="openReservation('UIC Platform & Mobility');return false;">Reserve</a>
                        </td>
                        <td>Administrative support, general IT access, local workshops, and presentations.</td>
                        <td>Laptop Computers, Multi-function Printers, Wi-Fi Access Points, Portable Sound Systems (battery powered).</td>
                    </tr>
                    <tr>
                        <td>
                            <strong>Foundational Prototyping</strong>
                            <a href="#" class="reserve-link" onclick="openReservation('Foundational Prototyping');return false;">Reserve</a>
                        </td>
                        <td>Preliminary testing in food processing, basic electronics, and light fabrication/repair.</td>
                        <td>Gas cooker (4 burners), Food processer (750W), Benchtop sealer, SMD Station, Digital Multimeter, Electric Drill, Welding Plant, Tool Box.</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>

    <!-- Reservation Modal Popup -->
    <div id="reservation-modal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeReservation()">&times;</span>
            <h3 style="margin-top:0;">Reserve Facility</h3>
            <form id="reservation-form" onsubmit="submitReservation(event)">
                <input type="hidden" name="facility" id="facility-input">
                <label for="user-name">Your Name *</label>
                <input type="text" id="user-name" name="user-name" required>

                <label for="user-email">Email *</label>
                <input type="email" id="user-email" name="user-email" required>

                <label for="reservation-date">Date of Use *</label>
                <input type="date" id="reservation-date" name="reservation-date" required>

                <label for="reservation-time">Time Slot *</label>
                <input type="text" id="reservation-time" name="reservation-time" placeholder="e.g., 9:00-12:00" required>
                
                <label for="purpose">Purpose or Notes</label>
                <textarea id="purpose" name="purpose" placeholder="Brief reason or special requirements..." rows="2"></textarea>

                <button type="submit">Submit Reservation</button>
                <div id="reservation-message"></div>
            </form>
        </div>
    </div>

    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tabbuttons;
            tabcontent = document.getElementsByClassName("tab-content");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }
            tabbuttons = document.getElementsByClassName("tab-button");
            for (i = 0; i < tabbuttons.length; i++) {
                tabbuttons[i].className = tabbuttons[i].className.replace(" active", "");
            }
            document.getElementById(tabName).style.display = "block";
            evt.currentTarget.className += " active";
        }

        // Reservation modal logic
        function openReservation(facilityName) {
            document.getElementById('facility-input').value = facilityName;
            document.getElementById('reservation-form').reset();
            document.getElementById('reservation-message').innerText = '';
            document.getElementById('reservation-modal').style.display = "block";
            document.getElementById('user-name').focus();
        }
        function closeReservation() {
            document.getElementById('reservation-modal').style.display = "none";
        }
        // Simulate reservation "submit" (just UI, not backend-connected)
        function submitReservation(event) {
            event.preventDefault();
            // Optional: basic frontend validation here (already handled by 'required')
            document.getElementById('reservation-message').innerText = "Reservation submitted! (Demo only – this does not save your request.)";
            setTimeout(closeReservation, 2000);
        }
        // Modal dismiss on background click
        window.onclick = function(event) {
            if (event.target == document.getElementById('reservation-modal')) {
                closeReservation();
            }
        }
        // Optional: ESC key closes modal
        document.addEventListener('keydown', function(evt) {
            if (evt.key === "Escape") closeReservation();
        });
    </script>
</body>
</html>
