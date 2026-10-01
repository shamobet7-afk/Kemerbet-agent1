<style>
    :root {
        --primary-color: #ff6b00;
        --primary-hover: #e05d00;
        --bg-color: #ffffff;
        --card-bg: #f8fafc;
        --input-bg: #ffffff;
        --text-color: #0f172a;
        --text-muted: #64748b;
        --border-color: #cbd5e1;
        --danger-color: #ef4444;
        --success-color: #22c55e;
        --admin-bg: #ffffff;
    }

    * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
        font-family: 'Poppins', sans-serif;
    }

    body {
        background-color: var(--bg-color);
        color: var(--text-color);
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    /* Top Header */
    .header {
        width: 100%;
        background: linear-gradient(135deg, #f8fafc, #e2e8f0);
        border-bottom: 2px solid var(--primary-color);
        padding: 20px;
        text-align: center;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
        position: relative;
    }

    .header h1 {
        color: var(--primary-color);
        font-size: 28px;
        font-weight: 700;
        letter-spacing: 1px;
        text-transform: uppercase;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
    }

    .header p {
        color: var(--text-muted);
        font-size: 13px;
        margin-top: 4px;
    }

    .main-container {
        width: 100%;
        max-width: 480px;
        padding: 20px;
        margin-top: 20px;
    }

    /* Card Styling */
    .card {
        background-color: var(--card-bg);
        border-radius: 16px;
        padding: 28px;
        box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
        border: 1px solid var(--border-color);
        position: relative;
    }

    .card-title {
        font-size: 20px;
        font-weight: 600;
        margin-bottom: 20px;
        text-align: center;
        color: var(--text-color);
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
    }

    /* Input Fields */
    .input-group {
        margin-bottom: 18px;
        position: relative;
    }

    .input-group label {
        display: block;
        font-size: 13px;
        color: var(--text-muted);
        margin-bottom: 8px;
        font-weight: 500;
    }

    .input-wrapper {
        position: relative;
        display: flex;
        align-items: center;
    }

    .input-wrapper i.input-icon {
        position: absolute;
        left: 14px;
        color: var(--text-muted);
        font-size: 15px;
    }

    .input-wrapper input {
        width: 100%;
        padding: 12px 14px 12px 42px;
        background-color: var(--input-bg);
        border: 1.5px solid var(--border-color);
        border-radius: 10px;
        color: var(--text-color);
        font-size: 14px;
        outline: none;
        transition: all 0.3s ease;
    }

    .input-wrapper input:focus {
        border-color: var(--primary-color);
        box-shadow: 0 0 0 3px rgba(255, 107, 0, 0.15);
    }

    /* Toggle password visibility button */
    .toggle-pwd {
        position: absolute;
        right: 12px;
        background: none;
        border: none;
        color: var(--text-muted);
        cursor: pointer;
        font-size: 14px;
    }

    .toggle-pwd:hover {
        color: var(--text-color);
    }

    /* Buttons */
    .btn {
        width: 100%;
        padding: 12px;
        border: none;
        border-radius: 10px;
        font-size: 15px;
        font-weight: 600;
        cursor: pointer;
        transition: all 0.2s ease;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
    }

    .btn-primary {
        background-color: var(--primary-color);
        color: #ffffff;
        margin-top: 10px;
    }

    .btn-primary:hover {
        background-color: var(--primary-hover);
        transform: translateY(-1px);
    }

    .btn-primary:active {
        transform: translateY(0);
    }

    .btn-secondary {
        background-color: transparent;
        border: 1px solid var(--border-color);
        color: var(--text-muted);
        margin-top: 15px;
    }

    .btn-secondary:hover {
        background-color: #e2e8f0;
        color: var(--text-color);
    }

    .btn-danger {
        background-color: var(--danger-color);
        color: white;
        padding: 6px 10px;
        font-size: 12px;
        border-radius: 6px;
    }

    /* Message Notifications */
    .toast {
        padding: 12px 16px;
        border-radius: 8px;
        margin-bottom: 18px;
        font-size: 13px;
        display: none;
        align-items: center;
        gap: 10px;
    }

    .toast-success {
        background-color: rgba(34, 197, 94, 0.15);
        border: 1px solid var(--success-color);
        color: #15803d;
    }

    .toast-error {
        background-color: rgba(239, 68, 68, 0.15);
        border: 1px solid var(--danger-color);
        color: #b91c1c;
    }

    /* Admin Panel Modal Overlay */
    .modal-overlay {
        display: none;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.5);
        backdrop-filter: blur(4px);
        z-index: 100;
        justify-content: center;
        align-items: flex-start;
        padding: 20px;
        overflow-y: auto;
    }

    .admin-modal {
        background-color: var(--admin-bg);
        width: 100%;
        max-width: 800px;
        border-radius: 16px;
        border: 1px solid var(--border-color);
        padding: 25px;
        box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        margin-top: 30px;
    }

    .admin-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        padding-bottom: 15px;
        border-bottom: 1px solid var(--border-color);
    }

    .admin-title {
        font-size: 20px;
        color: var(--primary-color);
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .admin-actions {
        display: flex;
        gap: 10px;
    }

    /* Search Bar */
    .search-box {
        margin-bottom: 15px;
        position: relative;
    }

    .search-box input {
        width: 100%;
        padding: 10px 12px 10px 38px;
        background-color: var(--card-bg);
        border: 1px solid var(--border-color);
        border-radius: 8px;
        color: var(--text-color);
        outline: none;
        font-size: 13px;
    }

    .search-box i {
        position: absolute;
        left: 12px;
        top: 50%;
        transform: translateY(-50%);
        color: var(--text-muted);
    }

    /* Table Styling */
    .table-container {
        overflow-x: auto;
    }

    table {
        width: 100%;
        border-collapse: collapse;
        text-align: left;
        font-size: 13px;
    }

    th {
        background-color: var(--card-bg);
        color: var(--text-muted);
        padding: 12px;
        font-weight: 600;
        border-bottom: 2px solid var(--border-color);
    }

    td {
        padding: 12px;
        border-bottom: 1px solid var(--border-color);
        color: var(--text-color);
    }

    tr:hover {
        background-color: rgba(0, 0, 0, 0.02);
    }

    .pwd-cell {
        font-family: monospace;
        letter-spacing: 1px;
        background: rgba(0,0,0,0.05);
        padding: 4px 8px;
        border-radius: 4px;
    }

    .badge-time {
        font-size: 11px;
        color: var(--text-muted);
    }

    .empty-state {
        text-align: center;
        padding: 30px;
        color: var(--text-muted);
    }

    /* Auth Modal for Admin Passcode */
    .auth-card {
        max-width: 360px;
        margin: 100px auto;
    }

    /* Hidden Utility Class */
    .hidden {
        display: none !important;
    }
</style>
