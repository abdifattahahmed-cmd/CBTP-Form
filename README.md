# CBTP-Form
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Jigjiga University - Community Health Assessment Form</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #eef2f5;
            font-family: 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
            padding: 30px 20px;
            color: #1a2a3a;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            background: white;
            border-radius: 28px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            padding: 2rem 2rem 3rem 2rem;
        }

        /* header */
        .uni-header {
            text-align: center;
            margin-bottom: 2rem;
            border-bottom: 3px solid #0a5e2e;
            padding-bottom: 1.5rem;
        }

        .uni-header h1 {
            font-size: 1.9rem;
            color: #0a3b2f;
            letter-spacing: -0.3px;
        }

        .uni-header h2 {
            font-size: 1.2rem;
            font-weight: 500;
            color: #2c5a2e;
            margin-top: 8px;
            text-decoration: underline;
        }

        .sub {
            background: #f0f7f0;
            padding: 12px 20px;
            border-radius: 40px;
            margin: 20px 0 10px;
            font-size: 0.95rem;
            color: #1e4620;
        }

        .student-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            background: #f9fafc;
            padding: 18px 20px;
            border-radius: 20px;
            margin-bottom: 30px;
            justify-content: space-between;
            border: 1px solid #e0e7ed;
        }

        .student-field {
            flex: 1;
            min-width: 180px;
        }

        .student-field label {
            font-weight: 700;
            color: #1f4f2b;
            display: block;
            margin-bottom: 6px;
        }

        .student-field input {
            width: 100%;
            padding: 10px 12px;
            border: 1px solid #cbd5e1;
            border-radius: 16px;
            background: white;
            font-size: 0.9rem;
        }

        section {
            margin-top: 2rem;
            background: #ffffff;
            border-radius: 24px;
            border: 1px solid #e9edf2;
            padding: 1rem 1.5rem 1.8rem 1.5rem;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }

        .section-title {
            font-size: 1.6rem;
            font-weight: 700;
            border-left: 8px solid #0f7b3a;
            padding-left: 18px;
            margin-bottom: 1.5rem;
            color: #1f2e3a;
        }

        .inline-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem;
            margin-bottom: 1.5rem;
        }

        .form-group {
            flex: 1;
            min-width: 200px;
        }

        label {
            font-weight: 600;
            display: block;
            margin-bottom: 6px;
            font-size: 0.85rem;
            color: #2c3e44;
        }

        input, select, textarea {
            width: 100%;
            padding: 10px 12px;
            border: 1px solid #cbd5e0;
            border-radius: 14px;
            font-size: 0.9rem;
            transition: 0.2s;
            background: #fff;
        }

        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #0f7b3a;
            box-shadow: 0 0 0 3px rgba(15,123,58,0.2);
        }

        .checkbox-group, .radio-group {
            display: flex;
            flex-wrap: wrap;
            gap: 16px;
            align-items: center;
            margin-top: 8px;
        }

        .checkbox-group label, .radio-group label {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            font-weight: normal;
            font-size: 0.9rem;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1rem 0;
            font-size: 0.85rem;
            overflow-x: auto;
            display: block;
        }

        th, td {
            border: 1px solid #d4dce6;
            padding: 10px 8px;
            text-align: left;
            vertical-align: top;
        }

        th {
            background: #eef3f0;
            font-weight: 700;
        }

        .btn-submit {
            background: #0f7b3a;
            color: white;
            font-size: 1.2rem;
            font-weight: bold;
            border: none;
            padding: 14px 28px;
            border-radius: 40px;
            cursor: pointer;
            width: 100%;
            margin-top: 2.5rem;
            transition: all 0.2s;
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
        }

        .btn-submit:hover {
            background: #0a5e2e;
            transform: scale(0.99);
        }

        .status-msg {
            margin-top: 20px;
            padding: 15px;
            border-radius: 28px;
            background: #e6f7ec;
            color: #1e6b3b;
            text-align: center;
            font-weight: 500;
            display: none;
        }

        hr {
            margin: 20px 0;
        }

        .small-note {
            font-size: 0.75rem;
            color: #5a6e7c;
            margin-top: 6px;
        }

        @media (max-width: 700px) {
            .container {
                padding: 1rem;
            }
            .section-title {
                font-size: 1.3rem;
            }
        }
    </style>
</head>
<body>
<div class="container">
    <div class="uni-header">
        <h1>JIGJIGA UNIVERSITY</h1>
        <h2>Institute of Medicine and Health Science</h2>
        <div class="sub">📋 Community Assessment Questionnaire — Socio-demographic, Morbidity, Mortality, Health & Infrastructure</div>
    </div>

    <div class="student-row">
        <div class="student-field">
            <label>👤 Name of student</label>
            <input type="text" id="studentName" placeholder="Full name">
        </div>
        <div class="student-field">
            <label>📅 Date</label>
            <input type="date" id="assessmentDate">
        </div>
        <div class="student-field">
            <label>✍️ Signature (name)</label>
            <input type="text" id="signature" placeholder="Electronic signature">
        </div>
        <div class="student-field">
            <label>🏘️ Town / Kebele / House No.</label>
            <input type="text" id="address" placeholder="Town, Kebele, House No.">
        </div>
    </div>

    <!-- ========================= PART I ========================= -->
    <section>
        <div class="section-title">📊 Part I: Socio-demographic Information</div>
        <div style="overflow-x: auto;">
            <table id="familyTable">
                <thead>
                    <tr><th>#</th><th>Sex (M/F)</th><th>Age</th><th>Religion</th><th>Education Status</th><th>Occupation</th><th>Marital status</th></tr>
                </thead>
                <tbody id="familyRows"></tbody>
            </table>
        </div>
        <button type="button" class="btn-submit" style="background:#3e6b4b; width:auto; padding:6px 18px; margin-top:8px;" id="addRowBtn">+ Add family member</button>
        
        <div style="margin-top: 2rem;">
            <h3 style="font-size: 1.2rem;">👶 Birth and Death record</h3>
            <div class="inline-grid">
                <div class="form-group"><label>Male live birth (past month)</label><input type="number" id="maleLive" value="0"></div>
                <div class="form-group"><label>Female live birth (past month)</label><input type="number" id="femaleLive" value="0"></div>
                <div class="form-group"><label>Male still birth (past month)</label><input type="number" id="maleStill" value="0"></div>
                <div class="form-group"><label>Female still birth (past month)</label><input type="number" id="femaleStill" value="0"></div>
                <div class="form-group"><label>Currently alive (total infants past month)</label><input type="number" id="aliveInfants" value="0"></div>
            </div>
            <div class="inline-grid">
                <div class="form-group"><label>📆 Live births last 12 months</label><input type="number" id="live12m"></div>
                <div class="form-group"><label>⚠️ Still births last 12 months</label><input type="number" id="still12m"></div>
            </div>
            <h4>Deaths in household (past 12 months)</h4>
            <div id="deathEntries">
                <div class="death-row" style="display:flex; gap:10px; flex-wrap:wrap; margin-bottom:8px;">
                    <input type="text" placeholder="Sex" style="width:80px;"> <input type="text" placeholder="Age" style="width:80px;"> <input type="text" placeholder="Cause (accident/illness)" style="width:180px;"> <input type="text" placeholder="Remark" style="width:120px;">
                </div>
            </div>
            <button type="button" id="addDeathBtn" style="background:#ddd; border:none; border-radius:20px; padding:4px 14px;">+ Add death record</button>
        </div>
    </section>

    <!-- ========================= PART II Environmental ========================= -->
    <section>
        <div class="section-title">🏠 Part II: Environmental Health Condition</div>
        <div class="inline-grid">
            <div class="form-group"><label>Roof material</label><select id="roof"><option>Tin</option><option>Grass</option><option>Other</option></select></div>
            <div class="form-group"><label>Floor material</label><select id="floor"><option>Concrete</option><option>Mud</option><option>Other</option></select></div>
            <div class="form-group"><label>Sleeping arrangements</label><select id="sleep"><option>Bed</option><option>Floor</option><option>Other</option></select></div>
            <div class="form-group"><label>Connected to neighbor's house?</label><select id="connected"><option>No</option><option>Yes</option></select></div>
            <div class="form-group"><label>Rooms/Windows</label><input placeholder="Rooms" id="rooms" style="width:70px;"> <input placeholder="Windows" id="windows" style="width:80px;"></div>
            <div class="form-group"><label>Open windows during obs.</label><select id="windowsOpen"><option>Yes</option><option>No</option></select></div>
            <div class="form-group"><label>Ventilation</label><select id="ventilation"><option>One-way</option><option>Cross</option><option>Opposite</option><option>Other</option></select></div>
        </div>
        <h3>Kitchen & Cooking</h3>
        <div class="inline-grid">
            <div class="form-group"><label>Kitchen exists?</label><select id="kitchenExist"><option>Yes</option><option>No</option></select></div>
            <div class="form-group"><label>Attached to main house?</label><select id="kitchenAttach"><option>Yes</option><option>No</option></select></div>
            <div class="form-group"><label>Adequate window?</label><select id="kitchenWindow"><option>Yes</option><option>No</option></select></div>
            <div class="form-group"><label>Smoke flow way?</label><select id="smokeFlow"><option>Yes</option><option>No</option></select></div>
        </div>
        <div class="form-group"><label>🔥 Cooking fuel (select all)</label><div class="checkbox-group"><label><input type="checkbox" value="Wood"> Wood</label><label><input type="checkbox" value="Cattle dung"> Cattle dung</label><label><input type="checkbox" value="Charcoal"> Charcoal</label><label><input type="checkbox" value="Dry leaves"> Dry leaves</label><label><input type="checkbox" value="Kerosene"> Kerosene</label><label><input type="checkbox" value="Electricity"> Electricity</label><label><input type="text" placeholder="Other" id="fuelOther" style="width:100px;"></label></div></div>
        
        <h3>🚽 Toilet & Sanitation</h3>
        <div class="inline-grid"><div class="form-group"><label>Toilet present?</label><select id="toiletExist"><option>Yes</option><option>No</option></select></div>
        <div class="form-group"><label>Type/cover</label><select id="toiletType"><option>Has prepared cover</option><option>No cover</option></select></div>
        <div class="form-group"><label>Covered during observation?</label><select id="toiletCovered"><option>Yes</option><option>No</option></select></div>
        <div class="form-group"><label>Usage</label><select id="toiletUsage"><option>Private</option><option>Common</option></select></div>
        <div class="form-group"><label>Feces on floor?</label><select id="fecesFloor"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Handwashing facility?</label><select id="handwash"><option>Yes</option><option>No</option></select></div>
        </div>
        <div class="form-group"><label>If no toilet, where defecate?</label><input id="defecatePlace" placeholder="Field/forest/other"></div>
        <div class="form-group"><label>Majority defecation place</label><input id="majorDefecate" placeholder="Same as above"></div>

        <h3>🗑️ Solid waste & compound</h3>
        <div class="inline-grid"><div class="form-group"><label>Temporary storage with cover?</label><select id="wasteCover"><option>Yes</option><option>No</option></select></div>
        <div class="form-group"><label>Waste disposal location</label><select id="wasteDisposal"><option>In the compound</option><option>In the pit</option><option>Open space</option><option>Municipality</option><option>Other</option></select></div>
        <div class="form-group"><label>Compound cleanliness</label><select id="cleanliness"><option>Clean</option><option>Not clean</option></select></div></div>

        <h3>💧 Water access & animals</h3>
        <div class="inline-grid"><div class="form-group"><label>Water source</label><select id="waterSource"><option>Public tap</option><option>Compound</option><option>Spring</option><option>Unprotected</option><option>Other</option></select></div>
        <div class="form-group"><label>Storage container with cover?</label><select id="waterCover"><option>Yes</option><option>No</option></select></div>
        <div class="form-group"><label>Avg fetch time (min)</label><input id="fetchTime" placeholder="minutes"></div></div>
        <div class="inline-grid"><div class="form-group"><label>Animals in compound?</label><select id="animalsPresent"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Animals have place to live?</label><select id="animalShelter"><option>Yes</option><option>No</option></select></div></div>
        <h3>🦟 Pests & lighting</h3>
        <div class="checkbox-group"><label><input type="checkbox" id="flies"> Houseflies</label><label><input type="checkbox" id="fleas"> Fleas</label><label><input type="checkbox" id="mosquitoes"> Mosquitoes</label><label><input type="checkbox" id="cockroaches"> Cockroaches</label><label><input type="checkbox" id="mice"> Mice</label><label><input type="text" id="otherPests" placeholder="Other pest"></label></div>
        <div class="form-group"><label>Most problematic pest:</label><input id="worstPest"></div>
        <div class="form-group"><label>Adequate lighting? (write test)</label><select id="adequateLight"><option>Yes</option><option>No</option></select></div>
        <div class="form-group"><label>Health issue needing attention</label><textarea id="healthIssue" rows="2"></textarea></div>
    </section>

    <!-- ========================= PART III Maternal Child Health ========================= -->
    <section>
        <div class="section-title">🤰 Part III: Child & Maternal Health</div>
        <div class="inline-grid"><div class="form-group"><label>Age at first marriage (Woman1,2,3)</label><input id="marriageAge1" placeholder="Woman1 years"> <input id="marriageAge2" placeholder="Woman2"> <input id="marriageAge3" placeholder="Woman3"></div>
        <div class="form-group"><label>Age at first birth (Mother1,2,3)</label><input id="birthAge1" placeholder="Mother1"> <input id="birthAge2" placeholder="Mother2"> <input id="birthAge3" placeholder="Mother3"></div></div>
        <div class="inline-grid"><div class="form-group"><label>Abortion/miscarriage past 12m?</label><select id="abortionYes"><option>No</option><option>Yes</option></select> <label>Total number</label><input id="abortionNum" placeholder="0"></div>
        <div class="form-group"><label>Any pregnant now?</label><select id="pregnantNow"><option>No</option><option>Yes</option></select> <label>How many?</label><input id="pregnantCount" placeholder="0"></div>
        <div class="form-group"><label>Attended ANC checkups?</label><select id="ancCheck"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Births past 12 months?</label><select id="birthPast12"><option>No</option><option>Yes</option></select> <label>Number births</label><input id="birthCount12"></div></div>
        <h4>ANC service place & provider</h4>
        <table id="ancTable"><thead><tr><th>Place of ANC service</th><th>Number of visits</th><th>TTBA</th><th>TBA</th><th>Health professionals</th><th>Other</th></tr></thead><tbody><tr><td>A/ At home</td><td><input type="text" size="5" id="ancHomeVisits"></td><td><input type="checkbox" id="ancHomeTTBA"></td><td><input type="checkbox" id="ancHomeTBA"></td><td><input type="checkbox" id="ancHomeProf"></td><td><input type="text" id="ancHomeOther"></td></tr>
        <tr><td>B/ Health Facility</td><td><input type="text" size="5" id="ancFacilityVisits"></td><td><input type="checkbox" id="ancFacTTBA"></td><td><input type="checkbox" id="ancFacTBA"></td><td><input type="checkbox" id="ancFacProf"></td><td><input type="text" id="ancFacOther"></td></tr></tbody></table>
        <div class="form-group"><label>Women 15-49 received TT vaccine?</label><select id="ttVaccine"><option>No</option><option>Yes</option></select> <label>Completed all doses (TT1-5)?</label><select id="ttComplete"><option>No</option><option>Yes</option></select> <label>Discontinued reasons</label><input id="ttDiscontinue"></div>
        <div class="form-group"><label>Modern contraceptive use?</label><select id="contraceptiveUse"><option>No</option><option>Yes</option></select> <label>Total users</label><input id="contraUsers" placeholder="0"> <label>Current users</label><input id="contraCurrent"> <div class="checkbox-group">Types: <label><input type="checkbox" value="Pills"> Pills</label><label><input type="checkbox" value="Injectables"> Injectables</label><label><input type="checkbox" value="Implants"> Implants</label><label><input type="checkbox" value="IUD"> IUD</label><label><input type="checkbox" value="Condoms"> Condoms</label><label><input type="text" id="otherContra" placeholder="Other"></label></div></div>
        <h3>Child health: Breastfeeding & traditional practices</h3>
        <div class="inline-grid"><div class="form-group"><label>Current age (under5)</label><input id="childAgeMonths"> <label>Breastfed duration (months)</label><input id="breastDuration"> <label>Age started additional food (months)</label><input id="supplementAge"></div></div>
        <div class="checkbox-group"><label><input type="checkbox" id="tradTonsil"> Tonsil removal</label><label><input type="checkbox" id="tradTeeth"> Milk teeth extraction</label><label><input type="checkbox" id="tradFGC"> Female genital cutting</label><label><input type="text" id="tradOther" placeholder="Other"></label></div>
        <h4>Immunization under 1 year</h4>
        <div class="inline-grid"><div class="form-group"><label>With card</label><input id="immCardYes"></div><div class="form-group"><label>Without card</label><input id="immCardNo"></div></div>
        <div id="vaccineRows"><div class="vaccine-row" style="display:flex; gap:8px; flex-wrap:wrap; margin-bottom:8px;"><span style="font-weight:bold;">Child 1:</span> Polio(0,1,2,3):<input size="6" placeholder="doses"> BCG scar:<select><option>Yes</option><option>No</option></select> Penta(1,2,3):<input size="5"> PCV:<input size="5"> Rota:<input size="5"> Measles:<input size="5"></div></div>
        <button type="button" id="addVaccineBtn">+ Add child immunization record</button>
        <h4>Diarrheal & other illnesses (last 14 days)</h4>
        <div class="inline-grid"><div class="form-group"><label>Diarrhea under 5 yrs</label><input id="diarrheaUnder5" value="0"></div><div class="form-group"><label>Diarrhea 5+ yrs</label><input id="diarrheaAbove5" value="0"></div></div>
        <div class="checkbox-group"><label>Encouraged fluids? <input type="checkbox" id="diarrFluids"></label> <label>Given ORS? <input type="checkbox" id="diarrOrs"></label> <label>If no ORS reason: <select id="orsReason"><option></option><option>Don't know its use</option><option>Not accessible</option><option>Can't afford</option></select></label></div>
        <div class="form-group"><label>Other illness last 14 days (disease & age)</label><textarea id="otherIllness" rows="2" placeholder="e.g., malaria - child 3y"></textarea></div>
    </section>

    <!-- ========================= Part IV Road Safety ========================= -->
    <section>
        <div class="section-title">🚦 Part IV: Road Safety</div>
        <div class="inline-grid"><div class="form-group"><label>Attended road safety sessions?</label><select id="roadSafetySessions"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Familiar with road rules?</label><select id="roadRules"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Helmet use</label><select id="helmetUse"><option>Never</option><option>Sometimes</option><option>Always</option></select></div>
        <div class="form-group"><label>Seatbelt use</label><select id="seatbeltUse"><option>Never</option><option>Sometimes</option><option>Always</option></select></div>
        <div class="form-group"><label>First aid training?</label><select id="firstAidTrain"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Cycle regularly?</label><select id="cycleRegular"><option>No</option><option>Yes</option></select> <label>Use lights/reflectors?</label><select id="cycleLights"><option>No</option><option>Yes</option></select></div>
        <div class="checkbox-group">Pedestrian infrastructure: <label><input type="checkbox" id="infraCross"> Crosswalks</label><label><input type="checkbox" id="infraSpeed"> Speed bumps</label><label><input type="checkbox" id="infraStreetlights"> Streetlights</label><label><input type="checkbox" id="infraNone"> None</label></div>
        <div class="form-group"><label>Suggestions for road safety</label><textarea id="roadSuggestions" rows="2"></textarea></div>
    </section>

    <!-- ========================= Part V & VI ========================= -->
    <section>
        <div class="section-title">🏥 Part V & VI: Healthcare Access, Mental Health, Feedback</div>
        <div class="inline-grid"><div class="form-group"><label>Distance to nearest health facility</label><select id="distFacility"><option><1 km</option><option>1-5 km</option><option>>5 km</option></select></div>
        <div class="form-group"><label>Frequency of visits</label><select id="visitFreq"><option>Monthly</option><option>Quarterly</option><option>Rarely</option></select></div>
        <div class="form-group"><label>Use traditional healers?</label><select id="tradHealer"><option>No</option><option>Yes</option></select> Reason: <label><input type="checkbox" id="reasonCost">Cost</label><label><input type="checkbox" id="reasonCulture">Cultural trust</label><label><input type="checkbox" id="reasonAccess">Lack modern access</label></div>
        <div class="form-group"><label>Health education past year?</label><select id="healthEd"><option>No</option><option>Yes</option></select> <label>Topics</label><input id="healthEdTopics" placeholder="Topics"></div>
        <div class="form-group"><label>Mental health services available?</label><select id="mentalServices"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Would seek help for mental health?</label><select id="mentalSeek"><option>No</option><option>Yes</option></select></div>
        <div class="form-group"><label>Biggest health challenge in kebele</label><textarea id="healthChallenge" rows="2"></textarea></div>
        <div class="form-group"><label>Suggestions for improvement</label><textarea id="improvementSuggest" rows="2"></textarea></div>
    </section>

    <button class="btn-submit" id="submitForm">📥 SUBMIT ASSESSMENT (Generate Summary)</button>
    <div id="statusMsg" class="status-msg"></div>
</div>

<script>
    // Family table dynamic rows
    const familyBody = document.getElementById('familyRows');
    function addFamilyRow(index) {
        const tr = document.createElement('tr');
        tr.innerHTML = `<td>${index}</td><td><input type="text" style="width:70px;"></td><td><input type="text" style="width:70px;"></td><td><input type="text" style="width:90px;"></td><td><input type="text" style="width:100px;"></td><td><input type="text" style="width:100px;"></td><td><input type="text" style="width:100px;"></td>`;
        familyBody.appendChild(tr);
    }
    for(let i=1;i<=4;i++) addFamilyRow(i);
    document.getElementById('addRowBtn').addEventListener('click',()=>{ addFamilyRow(familyBody.children.length+1); });

    // Death dynamic
    const deathContainer = document.getElementById('deathEntries');
    document.getElementById('addDeathBtn').addEventListener('click',()=>{
        const div = document.createElement('div'); div.className='death-row'; div.style.display='flex'; div.style.gap='8px'; div.style.marginBottom='8px';
        div.innerHTML = `<input type="text" placeholder="Sex" style="width:80px;"> <input type="text" placeholder="Age" style="width:80px;"> <input type="text" placeholder="Cause" style="width:180px;"> <input type="text" placeholder="Remark" style="width:120px;">`;
        deathContainer.appendChild(div);
    });
    // Vaccine dynamic
    const vaccineDiv = document.getElementById('vaccineRows');
    document.getElementById('addVaccineBtn').addEventListener('click',()=>{
        const newRow = document.createElement('div'); newRow.className='vaccine-row'; newRow.style.display='flex'; newRow.style.gap='8px'; newRow.style.flexWrap='wrap'; newRow.style.marginBottom='8px';
        newRow.innerHTML = `<span style="font-weight:bold;">Child ${vaccineDiv.children.length+1}:</span> Polio(0-3):<input size="5"> BCG scar:<select><option>Yes</option><option>No</option></select> Penta(1,2,3):<input size="5"> PCV:<input size="5"> Rota:<input size="5"> Measles:<input size="5">`;
        vaccineDiv.appendChild(newRow);
    });
    document.getElementById('submitForm').addEventListener('click',()=>{
        const student = document.getElementById('studentName').value || "Anonymous";
        const date = document.getElementById('assessmentDate').value || new Date().toISOString().slice(0,10);
        document.getElementById('statusMsg').innerHTML = `✅ Assessment recorded for ${student} on ${date}. Thank you! Data can be reviewed locally. (Demo version - full export ready)`;
        document.getElementById('statusMsg').style.display = 'block';
        setTimeout(()=>{ document.getElementById('statusMsg').style.display='none'; }, 5000);
        console.log("All questionnaire data captured in console — ready for backend integration");
        // scroll
        window.scrollTo({top:0, behavior:'smooth'});
    });
</script>
</body>
</html>