<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EHEPS Unified Portal | Microsoft Partner & Nonprofit Hub</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, BlinkMacSystemFont, Roboto, sans-serif;
            background: #f1f3f4;
            color: #202124;
            line-height: 1.5;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #0f2c3d 0%, #1a5f7a 100%);
            color: white;
            padding: 0.75rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }
        .logo {
            font-weight: 600;
            font-size: 1.1rem;
        }
        .user-info {
            background: rgba(255,255,255,0.2);
            padding: 0.3rem 0.9rem;
            border-radius: 30px;
            font-size: 0.85rem;
        }

        /* Tab navigation */
        .tabs {
            display: flex;
            flex-wrap: wrap;
            background: white;
            border-bottom: 1px solid #dadce0;
            padding: 0 1rem;
            gap: 0.5rem;
        }
        .tab {
            padding: 0.8rem 1.2rem;
            cursor: pointer;
            font-weight: 500;
            color: #5f6368;
            border-bottom: 2px solid transparent;
            transition: all 0.2s;
        }
        .tab.active {
            color: #1a73e8;
            border-bottom-color: #1a73e8;
        }
        .tab:hover {
            background: #f1f3f4;
        }

        /* Tab content */
        .tab-content {
            display: none;
            padding: 1.5rem;
            animation: fadeIn 0.3s ease;
        }
        .tab-content.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px);}
            to { opacity: 1; transform: translateY(0);}
        }

        /* General card styles */
        .card {
            background: white;
            border-radius: 16px;
            padding: 1.2rem;
            box-shadow: 0 1px 2px rgba(0,0,0,0.05);
            border: 1px solid #e4e7eb;
            margin-bottom: 1.5rem;
        }
        .card-header {
            font-weight: 600;
            margin-bottom: 1rem;
            border-bottom: 1px solid #e8eaed;
            padding-bottom: 0.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.5rem;
        }
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }
        .info-row {
            display: flex;
            justify-content: space-between;
            padding: 0.5rem 0;
            border-bottom: 1px solid #f0f0f0;
            font-size: 0.85rem;
        }
        .badge {
            background: #e6f4ea;
            color: #137333;
            padding: 0.2rem 0.6rem;
            border-radius: 20px;
            font-size: 0.7rem;
        }
        .badge-warning {
            background: #fef7e0;
            color: #b45f06;
        }
        .btn {
            background: #1a73e8;
            color: white;
            border: none;
            padding: 0.4rem 0.8rem;
            border-radius: 24px;
            font-size: 0.75rem;
            cursor: pointer;
        }
        .btn-outline {
            background: transparent;
            border: 1px solid #1a73e8;
            color: #1a73e8;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1rem;
        }
        .product-card {
            background: white;
            border-radius: 12px;
            padding: 1rem;
            border: 1px solid #e4e7eb;
        }
        .search-box {
            margin-bottom: 1rem;
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
        }
        .search-box input {
            flex: 1;
            padding: 0.5rem;
            border-radius: 30px;
            border: 1px solid #ccc;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.75rem;
        }
        th, td {
            text-align: left;
            padding: 0.5rem;
            border-bottom: 1px solid #e8eaed;
        }
        th {
            background: #f8f9fa;
            font-weight: 600;
        }
        footer {
            text-align: center;
            font-size: 0.7rem;
            color: #5f6368;
            padding: 1rem;
            border-top: 1px solid #e0e4e8;
            margin-top: 1rem;
        }
        .security-block {
            background: #f8f9fc;
            border-left: 4px solid #1a73e8;
            padding: 1rem;
            margin-top: 1rem;
            text-align: left;
            font-size: 0.7rem;
            font-family: 'Segoe UI', monospace;
            white-space: pre-wrap;
        }
        @media (max-width: 700px) {
            .tabs { overflow-x: auto; white-space: nowrap; flex-wrap: nowrap; }
            .tab { padding: 0.6rem 1rem; }
        }
    </style>
</head>
<body>
<div class="header">
    <div class="logo">🔷 EHEPS International Unified Portal</div>
    <div class="user-info">📧 executivedirector@eheps.org | ✅ Verified Nonprofit</div>
</div>

<div class="tabs" id="tabs">
    <div class="tab active" data-tab="partner">🏠 Partner Hub</div>
    <div class="tab" data-tab="subscriptions">📋 Subscriptions</div>
    <div class="tab" data-tab="offers">🎁 Product Offers</div>
    <div class="tab" data-tab="nonprofit">📘 Microsoft Nonprofit</div>
    <div class="tab" data-tab="endpoints">🌐 M365 Endpoints</div>
    <div class="tab" data-tab="entra">🔐 Entra ID</div>
    <div class="tab" data-tab="server">🖥️ cPanel Server</div>
</div>

<!-- ==================== PARTNER HUB TAB ==================== -->
<div id="partner" class="tab-content active">
    <div class="card">
        <div class="card-header">🏢 EHEPS organization · Account information</div>
        <div class="grid-2">
            <div>
                <div class="info-row"><span>Company</span><span>EHEPS organization</span></div>
                <div class="info-row"><span>Partner ID</span><span>ShuKjElxDO</span></div>
                <div class="info-row"><span>Legal address</span><span>822 W 23rd St, Unit A, Cheyenne, WY 82001</span></div>
            </div>
            <div>
                <div class="info-row"><span>Account domains</span><span>ehepso.com · eheps.com</span></div>
                <div class="info-row"><span>Account status</span><span><span class="badge">Manually verified</span></span></div>
                <div class="info-row"><span>Years in business</span><span>Unspecified</span></div>
            </div>
        </div>
    </div>
    <div class="card">
        <div class="card-header">📈 Partner Performance</div>
        <div class="grid-2">
            <div>Active opportunities: 3</div>
            <div>Workloads in progress: 2</div>
            <div>Earnings MTD: $0.00</div>
        </div>
    </div>
    <div class="card">
        <div class="card-header">📚 Resources</div>
        <ul><li>Google Partner Program Guide</li><li>Technical Support Hub</li><li>Certification & Training</li></ul>
    </div>
</div>

<!-- ==================== SUBSCRIPTIONS TAB ==================== -->
<div id="subscriptions" class="tab-content">
    <div class="card">
        <div class="card-header">📋 Google & Microsoft Subscriptions</div>
        <div style="overflow-x: auto;">
            <table>
                <thead><tr><th>Name</th><th>Status</th><th>Licenses</th><th>Payment plan</th></tr></thead>
                <tbody>
                    <tr><td>Android Enterprise</td><td><span class="badge">Active</span></td><td>All licenses</td><td>Free</td></tr>
                    <tr><td>Chrome Enterprise Core</td><td><span class="badge">Active</span></td><td>All licenses</td><td>Free</td></tr>
                    <tr><td>Cloud Identity Free</td><td><span class="badge">Active</span></td><td>50 available</td><td>Free</td></tr>
                    <tr><td>Cloud Identity Premium</td><td><span class="badge">Active</span></td><td>0 avail, 1 assigned</td><td>Annual</td></tr>
                    <tr><td>Colab Pro+</td><td><span class="badge">Active</span></td><td>0 avail, 1 assigned</td><td>Monthly</td></tr>
                    <tr><td>Google Workspace Additional Storage (100GB)</td><td><span class="badge">Active</span></td><td>50 bundles</td><td>Monthly</td></tr>
                    <tr><td>Google Workspace Enterprise Plus</td><td><span class="badge">Active</span></td><td>0 avail, 10 assigned</td><td>Yearly</td></tr>
                    <tr><td>Kiosk & Signage Upgrade</td><td><span class="badge">Active</span></td><td>50 licenses</td><td>Monthly</td></tr>
                </tbody>
            </table>
        </div>
    </div>
</div>

<!-- ==================== PRODUCT OFFERS TAB ==================== -->
<div id="offers" class="tab-content">
    <div class="search-box">
        <input type="text" id="offerSearch" placeholder="🔍 Search offers...">
    </div>
    <div id="offersGrid" class="product-grid"></div>
</div>

<!-- ==================== MICROSOFT NONPROFIT TAB ==================== -->
<div id="nonprofit" class="tab-content">
    <div class="card" style="background: linear-gradient(135deg,#0b5a7e,#1e7e34); color:white;">
        <h2>🎉 $50,000 Startup Grant Awarded</h2>
        <p>Microsoft verified nonprofit – Azure credits + Microsoft 365 + Power Apps</p>
    </div>
    <div class="grid-2">
        <div class="card"><h3>Nonprofit data solutions in Microsoft Fabric</h3><p>Ingest, transform, visualize fundraising insights.</p></div>
        <div class="card"><h3>Grant Management</h3><p>End-to-end grant cycle management.</p></div>
        <div class="card"><h3>Volunteer Management</h3><p>Recruit, onboard, retain volunteers.</p></div>
        <div class="card"><h3>Azure Landing Zone</h3><p>Secure migration to Azure.</p></div>
    </div>
</div>

<!-- ==================== M365 ENDPOINTS TAB ==================== -->
<div id="endpoints" class="tab-content">
    <div class="search-box">
        <input type="text" id="endpointSearch" placeholder="🔍 Filter by domain/IP/port...">
        <button class="btn" id="downloadJsonBtn">📥 Download JSON</button>
    </div>
    <div class="card">
        <div style="overflow-x: auto;">
            <table id="endpointsTable">
                <thead><tr><th>ID</th><th>Category</th><th>Addresses</th><th>Ports</th></tr></thead>
                <tbody id="endpointsBody"></tbody>
            </table>
        </div>
    </div>
</div>

<!-- ==================== ENTRA ID TAB ==================== -->
<div id="entra" class="tab-content">
    <div class="grid-2">
        <div class="card">
            <div class="card-header">👤 Basic info</div>
            <div class="info-row"><span>Display name</span><span>EHESPO</span></div>
            <div class="info-row"><span>User principal name</span><span>executivedirector@eheps.org</span></div>
            <div class="info-row"><span>Object ID</span><span>d678d0ae-311e-45c6-adff-075ad0ca2341</span></div>
            <div class="info-row"><span>Created</span><span>Apr 19, 2026</span></div>
            <div class="info-row"><span>Identities</span><span>admin@ehso.onmicrosoft.com</span></div>
        </div>
        <div class="card">
            <div class="card-header">🔐 Security</div>
            <div class="info-row"><span>Account status</span><span>✅ Enabled</span></div>
            <div class="info-row"><span>Risky user</span><span class="badge" style="background:#d83b01;color:white;">⚠️ At risk</span></div>
            <div class="info-row"><span>MFA status</span><span>Capable (3 methods)</span></div>
            <div class="info-row"><span>Last interactive sign-in</span><span>Jun 6, 2026, 4:26 PM</span></div>
            <div class="info-row"><span>Last non-interactive sign-in</span><span>Jun 6, 2026, 4:22 PM</span></div>
            <button class="btn" style="margin-top:0.5rem;">🔑 Manage MFA methods</button>
        </div>
    </div>
    <div class="grid-3">
        <div class="card"><div class="card-header">👥 Group memberships</div><div style="font-size:2rem;">5</div><button class="btn-outline btn">View groups</button></div>
        <div class="card"><div class="card-header">📱 Applications</div><div style="font-size:2rem;">46</div><button class="btn-outline btn">Review consent</button></div>
        <div class="card"><div class="card-header">🛡️ Assigned roles</div><div style="font-size:2rem;">80</div><button class="btn-outline btn">PIM settings</button></div>
    </div>
    <div class="card">
        <div class="card-header">📦 Assigned licenses</div>
        <div class="grid-2">
            <div><div class="info-row"><span>Microsoft 365 Business Premium</span><span>✅ Active</span></div>
            <div class="info-row"><span>Microsoft Entra ID P2</span><span>✅ Active</span></div>
            <div class="info-row"><span>Azure AD Premium P2</span><span>✅ Active</span></div></div>
            <div><div class="info-row"><span>Microsoft Intune</span><span>✅ Active</span></div>
            <div class="info-row"><span>Microsoft Defender for Cloud</span><span>✅ Active</span></div>
            <div class="info-row"><span>Power BI Pro</span><span>✅ Active</span></div></div>
        </div>
    </div>
    <div class="card">
        <div class="card-header">💻 Code solutions (PowerShell / Microsoft Graph)</div>
        <pre style="background:#1e1e1e;color:#9cdcfe;padding:0.8rem;border-radius:8px;overflow-x:auto;"># PowerShell: Get risky users
Connect-MgGraph -Scopes "IdentityRiskEvent.Read.All"
Get-MgRiskDetection -Filter "userPrincipalName eq 'executivedirector@eheps.org'"

# Graph API: Reset MFA methods
PATCH https://graph.microsoft.com/v1.0/users/d678d0ae-311e-45c6-adff-075ad0ca2341/authentication/methods
{
    "methods": ["microsoftAuthenticator", "sms", "voiceCall"]
}</pre>
        <button class="btn" onclick="copyCode()">📋 Copy PowerShell snippet</button>
    </div>
</div>

<!-- ==================== CPANEL SERVER TAB ==================== -->
<div id="server" class="tab-content">
    <div class="grid-2">
        <div class="card">
            <div class="card-header">📁 Account Information</div>
            <div class="info-row"><span>Current User</span><span>ehepxjyq</span></div>
            <div class="info-row"><span>Primary Domain</span><span>eheps.org</span></div>
            <div class="info-row"><span>Shared IP Address</span><span>198.187.29.152</span></div>
            <div class="info-row"><span>Home Directory</span><span>/home/ehepxjyq</span></div>
            <div class="info-row"><span>Last Login IP</span><span>216.131.72.18</span></div>
            <div class="info-row"><span>User Analytics</span><span class="badge-warning badge">Disabled</span></div>
            <div class="info-row"><span>Theme</span><span>jupiter</span></div>
        </div>
        <div class="card">
            <div class="card-header">🔒 SSL Certificate</div>
            <div class="info-row"><span>Status</span><span class="badge">Active</span></div>
            <div class="info-row"><span>Issuer</span><span>Let's Encrypt / AutoSSL</span></div>
            <div class="info-row"><span>Expires</span><span>90-day auto-renewal</span></div>
            <button class="btn" onclick="alert('SSL details: Active for eheps.org and *.eheps.org')">🔍 View Certificate</button>
        </div>
    </div>
    <div class="card">
        <div class="card-header">⚙️ Server Information</div>
        <pre style="background:#1e1e1e;color:#9cdcfe;padding:0.8rem;border-radius:8px;">OS: CloudLinux 8 | cPanel: 118.0.32
PHP: 8.2.12 | MySQL: 10.6.15-MariaDB
Disk Usage: 2.4 GB / 50 GB (4.8%)
Bandwidth: 1.2 GB / Unlimited
PHP Memory Limit: 256M | Max Execution: 300s</pre>
        <button class="btn" onclick="alert('Redirecting to cPanel...')">📂 Open cPanel</button>
    </div>
</div>

<footer>
    <p>© 2026 EHEPS International – executivedirector@eheps.org | All dashboards in one file</p>
    <div class="security-block">
        <!-- BEGIN MICROSOFT SECURITY.MD V1.0.0 BLOCK -->

        ## Security

        Microsoft takes the security of our software products and services seriously, which
        includes all source code repositories in our GitHub organizations.

        **Please do not report security vulnerabilities through public GitHub issues.**

        For security reporting information, locations, contact information, and policies,
        please review the latest guidance for Microsoft repositories at
        [https://aka.ms/SECURITY.md](https://aka.ms/SECURITY.md).

        <!-- END MICROSOFT SECURITY.MD BLOCK -->
    </div>
</footer>

<script>
    // Tab switching
    const tabs = document.querySelectorAll('.tab');
    const contents = document.querySelectorAll('.tab-content');
    tabs.forEach(tab => {
        tab.addEventListener('click', () => {
            const target = tab.getAttribute('data-tab');
            tabs.forEach(t => t.classList.remove('active'));
            tab.classList.add('active');
            contents.forEach(c => c.classList.remove('active'));
            document.getElementById(target).classList.add('active');
        });
    });

    // Product offers data
    const offers = [
        { title: "Adobe Acrobat Pro", desc: "Save 94% on document solution", offer: "94% off" },
        { title: "Zoom", desc: "50% off collaboration tools", offer: "50% off" },
        { title: "LinkedIn Fundraise", desc: "75% off Sales Navigator", offer: "75% off" },
        { title: "Claude AI", desc: "70% off AI assistant", offer: "~70% off" },
        { title: "Microsoft 365 Business Premium", desc: "75% off + Copilot Chat", offer: "75% off" },
        { title: "Microsoft Azure Grant", desc: "$2,000 yearly credits", offer: "$2k" },
        { title: "monday.com", desc: "10 free users + 70% off", offer: "10 free" },
        { title: "OpenAI ChatGPT", desc: "Team $8/user or 75% off Enterprise", offer: "75% off" },
        { title: "Hootsuite", desc: "60% off social media management", offer: "60% off" },
        { title: "Docusign", desc: "50% off IAM and 30% off eSignature", offer: "50% off" },
        { title: "Canva", desc: "100% free design tools", offer: "Free" }
    ];

    function renderOffers(filter = "") {
        const grid = document.getElementById('offersGrid');
        const filtered = offers.filter(o => o.title.toLowerCase().includes(filter) || o.desc.toLowerCase().includes(filter));
        grid.innerHTML = filtered.map(o => `<div class="product-card"><strong>${o.title}</strong><br>${o.desc}<br><span class="badge">${o.offer}</span></div>`).join('');
    }
    document.getElementById('offerSearch')?.addEventListener('input', e => renderOffers(e.target.value.toLowerCase()));
    renderOffers();

    // M365 endpoints (simplified subset)
    const endpoints = [
        { id: "1", category: "Optimize", addresses: "outlook.office365.com, 13.107.6.152/31", ports: "TCP:443" },
        { id: "31", category: "Optimize", addresses: "*.sharepoint.com, 13.107.136.0/22", ports: "TCP:443" },
        { id: "11", category: "Optimize", addresses: "52.112.0.0/14", ports: "UDP:3478-3481" },
        { id: "184", category: "Required", addresses: "*.cloud.microsoft", ports: "TCP:443" },
        { id: "46", category: "Allow", addresses: "*.officeapps.live.com, 13.107.6.171/32", ports: "TCP:443" }
    ];
    function renderEndpoints(filter = "") {
        const tbody = document.getElementById('endpointsBody');
        const filtered = endpoints.filter(e => e.id.includes(filter) || e.addresses.toLowerCase().includes(filter) || e.ports.includes(filter));
        tbody.innerHTML = filtered.map(e => `<tr><td>${e.id}</td><td>${e.category}</td><td>${e.addresses}</td><td>${e.ports}</td></tr>`).join('');
    }
    document.getElementById('endpointSearch')?.addEventListener('input', e => renderEndpoints(e.target.value.toLowerCase()));
    renderEndpoints();
    document.getElementById('downloadJsonBtn')?.addEventListener('click', () => {
        const dataStr = JSON.stringify(endpoints, null, 2);
        const blob = new Blob([dataStr], {type: "application/json"});
        const url = URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.href = url;
        a.download = "m365_endpoints.json";
        a.click();
        URL.revokeObjectURL(url);
    });

    // Copy PowerShell snippet
    function copyCode() {
        const code = `# PowerShell: Get risky users
Connect-MgGraph -Scopes "IdentityRiskEvent.Read.All"
Get-MgRiskDetection -Filter "userPrincipalName eq 'executivedirector@eheps.org'"

# Graph API: Reset MFA methods
PATCH https://graph.microsoft.com/v1.0/users/d678d0ae-311e-45c6-adff-075ad0ca2341/authentication/methods
{
    "methods": ["microsoftAuthenticator", "sms", "voiceCall"]
}`;
        navigator.clipboard.writeText(code);
        alert("✅ PowerShell / Graph code copied to clipboard!");
    }
</script>
</body>
</html>
