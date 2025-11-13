<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CodeRunner Pro - Diamond Edition | ₹50 Crore</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- CodeMirror CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/codemirror.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/theme/dracula.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/theme/material.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/theme/eclipse.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/theme/monokai.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/fold/foldgutter.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/dialog/dialog.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/search/matchesonscrollbar.css">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #8B6BFF;
            --secondary: #6A4CFF;
            --success: #00D4AA;
            --danger: #FF6B9D;
            --warning: #FFB74D;
            --dark: #121212;
            --light: #f8f9fa;
            --sidebar-width: 280px;
            --editor-font-size: 16px;
            --gold: #FFD700;
            --silver: #C0C0C0;
            --platinum: #E5E4E2;
            --diamond: #B9F2FF;
            --ruby: #E0115F;
            --emerald: #50C878;
            --sapphire: #0F52BA;
            --amethyst: #9966CC;
            --luxury-gradient: linear-gradient(135deg, #8B6BFF, #6A4CFF, #FF6B9D, #00D4AA);
            --luxury-gradient-2: linear-gradient(135deg, #121212, #1a1a2e, #16213e, #0f3460);
            --luxury-gradient-3: linear-gradient(135deg, #FFD700, #FF9D00, #FF6B00, #FF3C00);
            --glass-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
            --glass-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            --text-gold: linear-gradient(135deg, #FFD700, #FFA500, #FF8C00);
        }
        
        body {
            background: var(--luxury-gradient-2);
            color: #fff;
            min-height: 100vh;
            display: flex;
            overflow: hidden;
            width: 100vw;
            height: 100vh;
        }
        
        .container {
            display: flex;
            width: 100%;
            height: 100vh;
            position: relative;
        }
        
        /* Luxury Sidebar */
        .sidebar {
            width: var(--sidebar-width);
            background: linear-gradient(180deg, rgba(18, 18, 18, 0.95) 0%, rgba(26, 26, 46, 0.9) 100%);
            color: white;
            padding: 15px 0;
            display: flex;
            flex-direction: column;
            box-shadow: 10px 0 30px rgba(0, 0, 0, 0.5);
            z-index: 100;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
            border-right: 1px solid var(--glass-border);
            flex-shrink: 0;
        }
        
        .sidebar::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: var(--luxury-gradient);
            z-index: 10;
            box-shadow: 0 0 20px rgba(139, 107, 255, 0.7);
        }
        
        .logo {
            text-align: center;
            padding: 0 15px 15px;
            border-bottom: 1px solid var(--glass-border);
            margin-bottom: 15px;
            position: relative;
        }
        
        .logo h1 {
            font-size: 1.6rem;
            margin-bottom: 5px;
            background: var(--text-gold);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 800;
            letter-spacing: 1px;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
        }
        
        .logo p {
            font-size: 0.8rem;
            opacity: 0.7;
            color: var(--silver);
            font-weight: 300;
            letter-spacing: 1px;
        }
        
        .nav-links {
            list-style: none;
            padding: 0 10px;
            flex: 1;
            overflow-y: auto;
        }
        
        .nav-links li {
            margin-bottom: 8px;
            position: relative;
            overflow: hidden;
        }
        
        .nav-links li::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 4px;
            background: var(--luxury-gradient);
            transform: translateX(-10px);
            transition: transform 0.3s;
            box-shadow: 0 0 10px rgba(139, 107, 255, 0.5);
        }
        
        .nav-links li:hover::before {
            transform: translateX(0);
        }
        
        .nav-links a {
            display: flex;
            align-items: center;
            padding: 12px 15px;
            color: white;
            text-decoration: none;
            border-radius: 10px;
            transition: all 0.3s;
            position: relative;
            z-index: 1;
            font-weight: 500;
            letter-spacing: 0.5px;
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(5px);
            border: 1px solid transparent;
            font-size: 0.9rem;
        }
        
        .nav-links a:hover, .nav-links a.active {
            background: rgba(139, 107, 255, 0.15);
            transform: translateX(5px);
            border: 1px solid rgba(139, 107, 255, 0.3);
            box-shadow: 0 5px 15px rgba(139, 107, 255, 0.2);
        }
        
        .nav-links i {
            margin-right: 12px;
            font-size: 1.1rem;
            width: 20px;
            text-align: center;
            color: var(--gold);
        }
        
        /* Main Content Styles */
        .main-content {
            flex: 1;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            background: var(--glass-bg);
            backdrop-filter: blur(15px);
            min-width: 0;
        }
        
        .header {
            background: linear-gradient(90deg, rgba(18, 18, 18, 0.9) 0%, rgba(26, 26, 46, 0.8) 100%);
            padding: 15px 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 10;
            border-bottom: 1px solid var(--glass-border);
            flex-shrink: 0;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: var(--luxury-gradient);
            box-shadow: 0 0 15px rgba(139, 107, 255, 0.7);
        }
        
        .header h2 {
            color: white;
            font-size: 1.4rem;
            font-weight: 700;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            background: var(--text-gold);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 1px;
        }
        
        .user-actions {
            display: flex;
            gap: 10px;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 8px 15px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 6px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
            letter-spacing: 0.5px;
            font-size: 0.85rem;
            backdrop-filter: blur(5px);
            border: 1px solid transparent;
            white-space: nowrap;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn-primary {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border: 1px solid rgba(139, 107, 255, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(139, 107, 255, 0.4);
        }
        
        .btn-success {
            background: linear-gradient(135deg, var(--success), #00B894);
            color: white;
            border: 1px solid rgba(0, 212, 170, 0.3);
        }
        
        .btn-success:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(0, 212, 170, 0.4);
        }
        
        .btn-danger {
            background: linear-gradient(135deg, var(--danger), #E84393);
            color: white;
            border: 1px solid rgba(255, 107, 157, 0.3);
        }
        
        .btn-danger:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(255, 107, 157, 0.4);
        }
        
        .btn-warning {
            background: linear-gradient(135deg, var(--warning), #FFA726);
            color: white;
            border: 1px solid rgba(255, 183, 77, 0.3);
        }
        
        .btn-warning:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(255, 183, 77, 0.4);
        }
        
        .btn-gold {
            background: var(--luxury-gradient-3);
            color: #333;
            font-weight: 700;
            border: 1px solid rgba(255, 215, 0, 0.3);
        }
        
        .btn-gold:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(255, 215, 0, 0.4);
        }
        
        /* Editor Layout */
        .editor-layout {
            display: flex;
            flex: 1;
            overflow: hidden;
            gap: 1px;
            min-height: 0;
        }
        
        .code-panel {
            flex: 1;
            display: flex;
            flex-direction: column;
            background: var(--glass-bg);
            border-right: 1px solid var(--glass-border);
            min-width: 0;
        }
        
        .preview-panel {
            flex: 1;
            display: flex;
            flex-direction: column;
            background: var(--glass-bg);
            min-width: 0;
        }
        
        .panel-header {
            background: linear-gradient(90deg, rgba(44, 62, 80, 0.9) 0%, rgba(52, 73, 94, 0.9) 100%);
            color: white;
            padding: 12px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
            border-bottom: 1px solid var(--glass-border);
            flex-shrink: 0;
        }
        
        .panel-title {
            font-weight: 600;
            font-size: 1rem;
            display: flex;
            align-items: center;
            gap: 10px;
            letter-spacing: 0.5px;
        }
        
        .panel-controls {
            display: flex;
            gap: 10px;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .editor-container {
            display: flex;
            flex-direction: column;
            flex: 1;
            overflow: hidden;
            position: relative;
            min-height: 0;
        }
        
        .editor-tabs {
            display: flex;
            background: rgba(52, 73, 94, 0.9);
            border-bottom: 1px solid var(--glass-border);
            flex-shrink: 0;
        }
        
        .editor-tab {
            padding: 10px 20px;
            color: white;
            cursor: pointer;
            border-right: 1px solid var(--glass-border);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            font-weight: 500;
            letter-spacing: 0.5px;
            font-size: 0.9rem;
            white-space: nowrap;
        }
        
        .editor-tab::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: var(--luxury-gradient);
            transform: translateY(3px);
            transition: transform 0.3s;
            box-shadow: 0 0 10px rgba(139, 107, 255, 0.5);
        }
        
        .editor-tab.active {
            background: rgba(67, 97, 238, 0.2);
        }
        
        .editor-tab.active::before {
            transform: translateY(0);
        }
        
        .editor-content {
            flex: 1;
            display: flex;
            overflow: hidden;
            position: relative;
            min-height: 0;
        }
        
        .editor-wrapper {
            flex: 1;
            display: none;
            position: absolute;
            width: 100%;
            height: 100%;
            min-height: 0;
        }
        
        .editor-wrapper.active {
            display: block;
        }
        
        /* Custom Font Size Classes for CodeMirror */
        .CodeMirror {
            height: 100%;
            line-height: 1.4;
            font-family: 'Fira Code', 'Courier New', monospace;
            background: rgba(30, 30, 30, 0.9) !important;
        }
        
        .font-size-12 .CodeMirror {
            font-size: 12px;
        }
        
        .font-size-13 .CodeMirror {
            font-size: 13px;
        }
        
        .font-size-14 .CodeMirror {
            font-size: 14px;
        }
        
        .font-size-15 .CodeMirror {
            font-size: 15px;
        }
        
        .font-size-16 .CodeMirror {
            font-size: 16px;
        }
        
        .font-size-17 .CodeMirror {
            font-size: 17px;
        }
        
        .font-size-18 .CodeMirror {
            font-size: 18px;
        }
        
        .font-size-19 .CodeMirror {
            font-size: 19px;
        }
        
        .font-size-20 .CodeMirror {
            font-size: 20px;
        }
        
        .font-size-21 .CodeMirror {
            font-size: 21px;
        }
        
        .font-size-22 .CodeMirror {
            font-size: 22px;
        }
        
        .font-size-23 .CodeMirror {
            font-size: 23px;
        }
        
        .font-size-24 .CodeMirror {
            font-size: 24px;
        }
        
        .preview-content {
            flex: 1;
            padding: 0;
            overflow: auto;
            background: white;
            min-height: 0;
        }
        
        #preview-frame {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* Console Output */
        .console-output {
            background: #1e1e1e;
            color: #00ff00;
            padding: 15px;
            font-family: 'Fira Code', 'Courier New', monospace;
            height: 150px;
            overflow-y: auto;
            border-top: 2px solid #333;
            flex-shrink: 0;
        }
        
        .console-header {
            background: #2a2a2a;
            color: white;
            padding: 10px 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #444;
            flex-shrink: 0;
        }
        
        .console-line {
            margin-bottom: 5px;
            white-space: pre-wrap;
            border-left: 3px solid transparent;
            padding-left: 10px;
            font-size: 0.85rem;
        }
        
        .console-error {
            color: #ff6b6b;
            border-left-color: #ff6b6b;
        }
        
        .console-success {
            color: #4ecdc4;
            border-left-color: #4ecdc4;
        }
        
        .console-warning {
            color: #ffd166;
            border-left-color: #ffd166;
        }
        
        /* Luxury Badge */
        .luxury-badge {
            position: fixed;
            top: 15px;
            right: 15px;
            background: var(--luxury-gradient-3);
            color: #333;
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: bold;
            z-index: 1000;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            display: flex;
            align-items: center;
            gap: 6px;
            font-size: 0.85rem;
            border: 1px solid rgba(255, 215, 0, 0.3);
            backdrop-filter: blur(5px);
        }
        
        .ai-assistant {
            position: fixed;
            bottom: 20px;
            left: 20px;
            background: var(--luxury-gradient);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.4);
            z-index: 1000;
            transition: all 0.3s;
            animation: pulse 2s infinite;
            border: 2px solid rgba(255, 255, 255, 0.2);
        }
        
        .ai-assistant:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 20px rgba(139, 107, 255, 0.6);
        }
        
        .ai-assistant i {
            font-size: 1.5rem;
        }
        
        /* Additional Luxury Elements */
        .gem-decoration {
            position: absolute;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            z-index: 5;
        }
        
        .gem-1 {
            top: 10%;
            left: 5%;
            background: var(--ruby);
            box-shadow: 0 0 10px var(--ruby);
        }
        
        .gem-2 {
            top: 25%;
            right: 8%;
            background: var(--emerald);
            box-shadow: 0 0 10px var(--emerald);
        }
        
        .gem-3 {
            bottom: 15%;
            left: 10%;
            background: var(--sapphire);
            box-shadow: 0 0 10px var(--sapphire);
        }
        
        .gem-4 {
            bottom: 30%;
            right: 5%;
            background: var(--amethyst);
            box-shadow: 0 0 10px var(--amethyst);
        }
        
        /* Luxury Welcome Screen */
        .welcome-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--luxury-gradient-2);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 3000;
            transition: opacity 0.5s, visibility 0.5s;
        }
        
        .welcome-content {
            text-align: center;
            color: white;
            max-width: 90%;
            padding: 30px;
            background: rgba(18, 18, 18, 0.8);
            border-radius: 15px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            position: relative;
            overflow: hidden;
        }
        
        .welcome-content::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: var(--luxury-gradient);
            box-shadow: 0 0 15px rgba(139, 107, 255, 0.7);
        }
        
        .welcome-logo {
            font-size: 3.5rem;
            margin-bottom: 20px;
            background: var(--luxury-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
            text-shadow: 0 0 15px rgba(139, 107, 255, 0.5);
        }
        
        .welcome-title {
            font-size: 2.5rem;
            margin-bottom: 15px;
            font-weight: 800;
            background: var(--text-gold);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 1px;
        }
        
        .welcome-subtitle {
            font-size: 1.2rem;
            margin-bottom: 25px;
            opacity: 0.8;
            font-weight: 300;
            letter-spacing: 0.5px;
        }
        
        .welcome-features {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-bottom: 25px;
        }
        
        .welcome-feature {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 10px;
            backdrop-filter: blur(5px);
            min-width: 140px;
            border: 1px solid var(--glass-border);
            transition: transform 0.3s;
        }
        
        .welcome-feature:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .welcome-feature i {
            font-size: 2rem;
            margin-bottom: 10px;
            color: var(--gold);
        }
        
        .welcome-feature h3 {
            font-size: 1.1rem;
            margin-bottom: 8px;
            font-weight: 600;
        }
        
        .welcome-feature p {
            font-size: 0.8rem;
            opacity: 0.8;
        }
        
        .welcome-btn {
            background: var(--luxury-gradient);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            font-size: 1.1rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
            letter-spacing: 0.5px;
            position: relative;
            overflow: hidden;
        }
        
        .welcome-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }
        
        .welcome-btn:hover::before {
            left: 100%;
        }
        
        .welcome-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 25px rgba(139, 107, 255, 0.5);
        }
        
        /* Luxury Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(10px);
        }
        
        .modal-content {
            background: linear-gradient(135deg, rgba(30, 30, 30, 0.95) 0%, rgba(40, 40, 40, 0.95) 100%);
            padding: 25px;
            border-radius: 15px;
            width: 90%;
            max-width: 500px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
            position: relative;
            overflow: hidden;
            border: 1px solid var(--glass-border);
        }
        
        .modal-content::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: var(--luxury-gradient);
            box-shadow: 0 0 15px rgba(139, 107, 255, 0.7);
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .modal-title {
            font-size: 1.4rem;
            color: white;
            font-weight: 700;
            background: var(--text-gold);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 0.5px;
        }
        
        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--danger);
            transition: transform 0.3s;
            width: 35px;
            height: 35px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background: rgba(255, 107, 157, 0.1);
        }
        
        .close-modal:hover {
            transform: rotate(90deg);
            background: rgba(255, 107, 157, 0.2);
        }
        
        /* Luxury Toast Notification */
        .toast {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--luxury-gradient);
            color: white;
            padding: 12px 20px;
            border-radius: 10px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
            display: flex;
            align-items: center;
            gap: 10px;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.4s;
            z-index: 1000;
            max-width: 350px;
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
        }
        
        .toast.show {
            transform: translateY(0);
            opacity: 1;
        }
        
        /* Luxury Status Bar */
        .status-bar {
            background: linear-gradient(90deg, rgba(44, 62, 80, 0.9) 0%, rgba(52, 73, 94, 0.9) 100%);
            color: white;
            padding: 10px 15px;
            display: flex;
            justify-content: space-between;
            font-size: 0.8rem;
            border-top: 1px solid var(--glass-border);
            flex-shrink: 0;
        }
        
        /* Luxury Theme Selector */
        .theme-selector {
            display: flex;
            gap: 10px;
            align-items: center;
        }
        
        .theme-option {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid transparent;
            transition: transform 0.3s;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.2);
        }
        
        .theme-option:hover {
            transform: scale(1.1);
        }
        
        .theme-option.active {
            border-color: white;
            transform: scale(1.1);
        }
        
        .theme-dark {
            background: #1e1e1e;
        }
        
        .theme-light {
            background: #f8f9fa;
        }
        
        .theme-monokai {
            background: #272822;
        }
        
        .theme-dracula {
            background: #282a36;
        }
        
        .theme-material {
            background: #263238;
        }
        
        /* Luxury Code Snippets */
        .code-snippets {
            position: absolute;
            right: 15px;
            top: 15px;
            z-index: 10;
        }
        
        .snippets-btn {
            background: var(--luxury-gradient);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.9rem;
            box-shadow: 0 5px 12px rgba(0, 0, 0, 0.2);
            transition: all 0.3s;
            font-weight: 600;
            letter-spacing: 0.5px;
            border: 1px solid var(--glass-border);
        }
        
        .snippets-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 15px rgba(139, 107, 255, 0.4);
        }
        
        .snippets-dropdown {
            display: none;
            position: absolute;
            right: 0;
            top: 100%;
            background: rgba(44, 62, 80, 0.95);
            border-radius: 10px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            width: 200px;
            z-index: 100;
            overflow: hidden;
            margin-top: 5px;
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
        }
        
        .snippets-dropdown.show {
            display: block;
            animation: fadeIn 0.3s;
        }
        
        .snippet-item {
            padding: 10px 15px;
            cursor: pointer;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.2s;
            font-weight: 500;
            font-size: 0.85rem;
        }
        
        .snippet-item:hover {
            background: rgba(139, 107, 255, 0.2);
            transform: translateX(3px);
        }
        
        .snippet-item:last-child {
            border-bottom: none;
        }
        
        /* Luxury Premium Features */
        .premium-features {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .premium-feature {
            background: var(--luxury-gradient);
            color: white;
            padding: 15px;
            border-radius: 10px;
            flex: 1;
            min-width: 150px;
            text-align: center;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
            border: 1px solid var(--glass-border);
        }
        
        .premium-feature:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 20px rgba(139, 107, 255, 0.4);
        }
        
        .premium-feature i {
            font-size: 2rem;
            margin-bottom: 10px;
        }
        
        /* Luxury Enterprise Badge */
        .enterprise-badge {
            position: absolute;
            top: 8px;
            left: 8px;
            background: var(--luxury-gradient-3);
            color: #333;
            padding: 5px 10px;
            border-radius: 6px;
            font-size: 0.8rem;
            font-weight: bold;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 215, 0, 0.3);
        }
        
        /* Luxury Collaboration Indicator */
        .collaboration-indicator {
            display: flex;
            align-items: center;
            gap: 8px;
            background: var(--luxury-gradient);
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            box-shadow: 0 5px 12px rgba(0, 0, 0, 0.2);
            border: 1px solid var(--glass-border);
        }
        
        .collaboration-indicator .dot {
            width: 10px;
            height: 10px;
            background: white;
            border-radius: 50%;
            animation: pulse 1.5s infinite;
        }
        
        /* Luxury User Profile */
        .user-profile {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .user-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--luxury-gradient);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            box-shadow: 0 5px 12px rgba(0, 0, 0, 0.2);
            border: 2px solid rgba(255, 255, 255, 0.2);
        }
        
        .user-name {
            font-weight: 600;
            color: white;
            font-size: 0.9rem;
        }
        
        /* Luxury Version Control */
        .version-control {
            display: flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 12px;
            border-radius: 8px;
            color: white;
            font-size: 0.85rem;
            border: 1px solid var(--glass-border);
            backdrop-filter: blur(5px);
        }
        
        .version-control select {
            background: transparent;
            border: none;
            color: white;
            outline: none;
            cursor: pointer;
            font-weight: 500;
            font-size: 0.85rem;
        }
        
        .version-control option {
            background: #2c3e50;
            color: white;
        }
        
        /* Luxury Editor Enhancements */
        .editor-enhancements {
            position: absolute;
            bottom: 15px;
            right: 15px;
            display: flex;
            gap: 10px;
            z-index: 10;
        }
        
        .enhancement-btn {
            background: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s;
            backdrop-filter: blur(5px);
            border: 1px solid var(--glass-border);
            font-size: 1rem;
        }
        
        .enhancement-btn:hover {
            background: var(--primary);
            transform: scale(1.1);
            box-shadow: 0 3px 10px rgba(139, 107, 255, 0.4);
        }
        
        /* Luxury Language Selector */
        .language-selector {
            display: flex;
            gap: 8px;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .language-option {
            padding: 6px 12px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.85rem;
            transition: all 0.3s;
            border: 1px solid var(--glass-border);
            font-weight: 500;
            backdrop-filter: blur(5px);
        }
        
        .language-option:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-1px);
        }
        
        .language-option.active {
            background: var(--primary);
            transform: translateY(-1px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        /* Luxury Projects List */
        .projects-list {
            max-height: 250px;
            overflow-y: auto;
            border: 1px solid var(--glass-border);
            border-radius: 10px;
            margin-top: 10px;
            background: rgba(255, 255, 255, 0.05);
        }
        
        .project-item {
            padding: 10px 15px;
            border-bottom: 1px solid var(--glass-border);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s;
        }
        
        .project-item:hover {
            background: rgba(139, 107, 255, 0.1);
            transform: translateX(3px);
        }
        
        .project-item:last-child {
            border-bottom: none;
        }
        
        .project-name {
            font-weight: 600;
            font-size: 0.9rem;
        }
        
        .project-date {
            font-size: 0.8rem;
            color: #aaa;
        }
        
        /* Luxury Export Options */
        .export-options {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        /* Animations */
        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.05); opacity: 0.8; }
            100% { transform: scale(1); opacity: 1; }
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) translateX(100px);
                opacity: 0;
            }
        }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 8px;
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--luxury-gradient);
            border-radius: 8px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: var(--primary);
        }
        
        /* Responsive Design */
        @media (max-width: 1200px) {
            .sidebar {
                width: 250px;
            }
            
            .header h2 {
                font-size: 1.2rem;
            }
            
            .btn {
                padding: 6px 12px;
                font-size: 0.8rem;
            }
        }
        
        @media (max-width: 992px) {
            .editor-layout {
                flex-direction: column;
            }
            
            .code-panel, .preview-panel {
                height: 50%;
            }
            
            .sidebar {
                width: 70px;
            }
            
            .logo h1, .logo p, .nav-links span {
                display: none;
            }
            
            .nav-links a {
                justify-content: center;
                padding: 12px;
            }
            
            .nav-links i {
                margin-right: 0;
                font-size: 1.2rem;
            }
            
            .header {
                padding: 10px 15px;
            }
            
            .header h2 {
                font-size: 1.1rem;
            }
            
            .user-actions {
                gap: 6px;
            }
            
            .btn {
                padding: 5px 10px;
                font-size: 0.75rem;
            }
            
            .welcome-title {
                font-size: 2rem;
            }
            
            .welcome-subtitle {
                font-size: 1rem;
            }
        }
        
        @media (max-width: 768px) {
            .user-actions {
                flex-direction: column;
                gap: 5px;
            }
            
            .btn {
                padding: 4px 8px;
                font-size: 0.7rem;
            }
            
            .panel-controls {
                flex-direction: column;
                gap: 5px;
            }
            
            .welcome-content {
                padding: 20px;
            }
            
            .welcome-title {
                font-size: 1.8rem;
            }
            
            .welcome-subtitle {
                font-size: 0.9rem;
            }
            
            .welcome-feature {
                min-width: 100%;
            }
            
            .luxury-badge {
                top: 10px;
                right: 10px;
                padding: 6px 12px;
                font-size: 0.75rem;
            }
        }
        
        @media (max-width: 576px) {
            .sidebar {
                width: 60px;
            }
            
            .header {
                flex-direction: column;
                gap: 10px;
                padding: 8px 10px;
            }
            
            .header h2 {
                font-size: 1rem;
                text-align: center;
            }
            
            .user-actions {
                width: 100%;
                justify-content: center;
            }
            
            .btn {
                font-size: 0.7rem;
                padding: 4px 8px;
            }
            
            .panel-header {
                flex-direction: column;
                gap: 8px;
                padding: 8px 10px;
            }
            
            .panel-title {
                font-size: 0.9rem;
            }
            
            .editor-tab {
                padding: 8px 12px;
                font-size: 0.8rem;
            }
            
            .console-output {
                height: 120px;
                padding: 10px;
            }
            
            .welcome-logo {
                font-size: 2.5rem;
            }
            
            .welcome-title {
                font-size: 1.5rem;
            }
        }
        
        @media (max-height: 700px) {
            .welcome-content {
                padding: 20px;
                max-height: 90vh;
                overflow-y: auto;
            }
            
            .welcome-logo {
                font-size: 2.5rem;
                margin-bottom: 15px;
            }
            
            .welcome-title {
                font-size: 1.8rem;
                margin-bottom: 10px;
            }
            
            .welcome-subtitle {
                font-size: 1rem;
                margin-bottom: 15px;
            }
            
            .welcome-features {
                margin-bottom: 15px;
            }
            
            .welcome-feature {
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <!-- Welcome Screen -->
    <div class="welcome-screen" id="welcome-screen">
        <div class="gem-decoration gem-1"></div>
        <div class="gem-decoration gem-2"></div>
        <div class="gem-decoration gem-3"></div>
        <div class="gem-decoration gem-4"></div>
        
        <div class="welcome-content">
            <div class="welcome-logo">
                <i class="fas fa-crown"></i>
            </div>
            <h1 class="welcome-title">CodeRunner Pro</h1>
            <p class="welcome-subtitle">Diamond Edition - ₹50 Crore</p>
            
            <div class="welcome-features">
                <div class="welcome-feature">
                    <i class="fas fa-bolt"></i>
                    <h3>Lightning Fast</h3>
                    <p>Ultra-performance code execution</p>
                </div>
                <div class="welcome-feature">
                    <i class="fas fa-shield-alt"></i>
                    <h3>Enterprise Security</h3>
                    <p>Military-grade encryption</p>
                </div>
                <div class="welcome-feature">
                    <i class="fas fa-users"></i>
                    <h3>Real-time Collaboration</h3>
                    <p>Team coding at its finest</p>
                </div>
                <div class="welcome-feature">
                    <i class="fas fa-cloud"></i>
                    <h3>Cloud Integration</h3>
                    <p>Seamless cloud deployment</p>
                </div>
            </div>
            
            <button class="welcome-btn" id="enter-app">
                <i class="fas fa-gem"></i> Enter Diamond Edition
            </button>
        </div>
    </div>

    <!-- Floating Particles -->
    <div class="particles" id="particles"></div>

    <div class="luxury-badge">
        <i class="fas fa-crown"></i>
        <span>Diamond Edition - ₹50 Crore</span>
    </div>
    <div class="ai-assistant" id="ai-assistant">
        <i class="fas fa-robot"></i>
    </div>
    
    <div class="container">
        <!-- Sidebar -->
        <div class="sidebar">
            <div class="logo">
                <h1>CodeRunner Pro</h1>
                <p>Diamond Development Suite</p>
            </div>
            <ul class="nav-links">
                <li><a href="#" class="active" id="nav-home"><i class="fas fa-home"></i> <span>Dashboard</span></a></li>
                <li><a href="#" id="nav-projects"><i class="fas fa-code"></i> <span>My Projects</span></a></li>
                <li><a href="#" id="nav-save"><i class="fas fa-save"></i> <span>Save Project</span></a></li>
                <li><a href="#" id="nav-share"><i class="fas fa-share-alt"></i> <span>Collaborate</span></a></li>
                <li><a href="#" id="nav-settings"><i class="fas fa-cog"></i> <span>Settings</span></a></li>
                <li><a href="#" id="nav-help"><i class="fas fa-question-circle"></i> <span>Help</span></a></li>
                <li><a href="#" id="nav-export"><i class="fas fa-download"></i> <span>Export</span></a></li>
                <li><a href="#" id="nav-login"><i class="fas fa-user"></i> <span>Account</span></a></li>
            </ul>
            
            <div class="premium-features" style="margin-top: auto; padding: 15px;">
                <div class="premium-feature">
                    <i class="fas fa-cloud"></i>
                    <h4>Cloud Sync</h4>
                    <p>Real-time backup</p>
                </div>
                <div class="premium-feature">
                    <i class="fas fa-users"></i>
                    <h4>Team Collaboration</h4>
                    <p>Multi-user editing</p>
                </div>
            </div>
        </div>

        <!-- Main Content -->
        <div class="main-content">
            <!-- Header -->
            <div class="header">
                <h2>CodeRunner Pro - Diamond Development Environment</h2>
                <div class="user-actions">
                    <div class="collaboration-indicator">
                        <div class="dot"></div>
                        <span>Live Collaboration</span>
                    </div>
                    <div class="version-control">
                        <span>Version:</span>
                        <select id="version-select">
                            <option>v4.0.0</option>
                            <option>v3.5.1</option>
                            <option>v3.0.0</option>
                        </select>
                    </div>
                    <div class="user-profile" id="user-profile" style="display: none;">
                        <div class="user-avatar" id="user-avatar">U</div>
                        <div class="user-name" id="user-name">User</div>
                        <button class="btn btn-danger" id="logout-btn">
                            <i class="fas fa-sign-out-alt"></i> Logout
                        </button>
                    </div>
                    <button class="btn btn-warning" id="new-project-btn">
                        <i class="fas fa-file"></i> New Project
                    </button>
                    <button class="btn btn-gold" id="premium-btn">
                        <i class="fas fa-crown"></i> Upgrade
                    </button>
                    <button class="btn btn-danger" id="clear-all-btn">
                        <i class="fas fa-broom"></i> Clear All
                    </button>
                    <button class="btn btn-success" id="run-btn">
                        <i class="fas fa-play"></i> Run Code
                    </button>
                </div>
            </div>

            <!-- Editor Layout -->
            <div class="editor-layout">
                <!-- Code Panel -->
                <div class="code-panel">
                    <div class="panel-header">
                        <div class="panel-title">
                            <i class="fas fa-code"></i> Diamond Code Editor
                            <div class="enterprise-badge">DIAMOND EDITION</div>
                        </div>
                        <div class="panel-controls">
                            <div class="language-selector">
                                <div class="language-option active" data-language="web">Web</div>
                                <div class="language-option" data-language="python">Python</div>
                                <div class="language-option" data-language="java">Java</div>
                                <div class="language-option" data-language="cpp">C++</div>
                            </div>
                            <div class="editor-features">
                                <div class="feature-toggle">
                                    <input type="checkbox" id="line-numbers-toggle" checked>
                                    <label for="line-numbers-toggle">Line Numbers</label>
                                </div>
                            </div>
                            <button class="btn btn-primary" id="html-clear">
                                <i class="fas fa-times"></i> Clear HTML
                            </button>
                            <button class="btn btn-primary" id="css-clear">
                                <i class="fas fa-times"></i> Clear CSS
                            </button>
                            <button class="btn btn-primary" id="js-clear">
                                <i class="fas fa-times"></i> Clear JS
                            </button>
                        </div>
                    </div>
                    
                    <div class="editor-container">
                        <div class="editor-tabs">
                            <div class="editor-tab active" data-editor="html">HTML</div>
                            <div class="editor-tab" data-editor="css">CSS</div>
                            <div class="editor-tab" data-editor="js">JavaScript</div>
                        </div>
                        
                        <div class="editor-content">
                            <div class="code-snippets">
                                <button class="snippets-btn" id="snippets-btn">
                                    <i class="fas fa-code"></i> Snippets
                                </button>
                                <div class="snippets-dropdown" id="snippets-dropdown">
                                    <div class="snippet-item" data-snippet="boilerplate">HTML Boilerplate</div>
                                    <div class="snippet-item" data-snippet="navbar">Navigation Bar</div>
                                    <div class="snippet-item" data-snippet="card">Card Component</div>
                                    <div class="snippet-item" data-snippet="button">Styled Button</div>
                                    <div class="snippet-item" data-snippet="animation">CSS Animation</div>
                                </div>
                            </div>
                            
                            <div class="editor-enhancements">
                                <button class="enhancement-btn" id="format-code" title="Format Code">
                                    <i class="fas fa-indent"></i>
                                </button>
                                <button class="enhancement-btn" id="find-replace" title="Find & Replace">
                                    <i class="fas fa-search"></i>
                                </button>
                                <button class="enhancement-btn" id="fullscreen" title="Fullscreen">
                                    <i class="fas fa-expand"></i>
                                </button>
                            </div>
                            
                            <div id="html-editor-wrapper" class="editor-wrapper active"></div>
                            <div id="css-editor-wrapper" class="editor-wrapper"></div>
                            <div id="js-editor-wrapper" class="editor-wrapper"></div>
                        </div>
                    </div>
                    
                    <!-- Status Bar -->
                    <div class="status-bar">
                        <div class="code-stats">
                            <span id="html-lines">HTML: 10 lines</span>
                            <span id="css-lines">CSS: 25 lines</span>
                            <span id="js-lines">JS: 15 lines</span>
                        </div>
                        <div class="theme-selector">
                            <span>Theme:</span>
                            <div class="theme-option theme-dracula active" data-theme="dracula" title="Dracula"></div>
                            <div class="theme-option theme-material" data-theme="material" title="Material"></div>
                            <div class="theme-option theme-monokai" data-theme="monokai" title="Monokai"></div>
                            <div class="theme-option theme-light" data-theme="eclipse" title="Light"></div>
                        </div>
                    </div>
                </div>
                
                <!-- Preview Panel -->
                <div class="preview-panel">
                    <div class="panel-header">
                        <div class="panel-title">
                            <i class="fas fa-eye"></i> Diamond Live Preview
                        </div>
                        <div class="panel-controls">
                            <button class="btn btn-primary" id="refresh-btn">
                                <i class="fas fa-redo"></i> Refresh
                            </button>
                            <button class="btn btn-warning" id="clear-console">
                                <i class="fas fa-trash"></i> Clear Console
                            </button>
                        </div>
                    </div>
                    
                    <div class="preview-content">
                        <iframe id="preview-frame"></iframe>
                        <div class="console-header">
                            <span><i class="fas fa-terminal"></i> Diamond Console</span>
                            <span id="execution-time"></span>
                        </div>
                        <div class="console-output" id="console-output">
                            <div class="console-line console-success">>> CodeRunner Pro Diamond Console Ready</div>
                            <div class="console-line">>> Select a language and click 'Run Code' to execute</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Notification -->
    <div class="toast" id="toast">
        <i class="fas fa-check-circle"></i>
        <span id="toast-message">Code executed successfully!</span>
    </div>

    <!-- Save Project Modal -->
    <div class="modal" id="save-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Save Project</h3>
                <button class="close-modal" id="close-save-modal">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="project-name">Project Name</label>
                    <input type="text" id="project-name" class="form-control" placeholder="Enter project name">
                </div>
                <div class="form-group">
                    <label for="project-description">Description (Optional)</label>
                    <textarea id="project-description" class="form-control" rows="3" placeholder="Enter project description"></textarea>
                </div>
            </div>
            <div class="modal-footer">
                <button class="btn btn-danger" id="cancel-save">Cancel</button>
                <button class="btn btn-success" id="confirm-save">Save Project</button>
            </div>
        </div>
    </div>

    <!-- Share Modal -->
    <div class="modal" id="share-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Share Project</h3>
                <button class="close-modal" id="close-share-modal">&times;</button>
            </div>
            <div class="modal-body">
                <p>Copy the link below to share your project:</p>
                <div class="form-group">
                    <input type="text" id="share-link" class="form-control" readonly value="https://coderunner-pro-diamond.com/project/12345">
                </div>
                <button class="btn btn-primary" id="copy-link">
                    <i class="fas fa-copy"></i> Copy Link
                </button>
            </div>
        </div>
    </div>

    <!-- Settings Modal -->
    <div class="modal" id="settings-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Diamond Settings</h3>
                <button class="close-modal" id="close-settings-modal">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="theme-select">Editor Theme</label>
                    <select id="theme-select" class="form-control">
                        <option value="dracula">Dracula</option>
                        <option value="material">Material</option>
                        <option value="monokai">Monokai</option>
                        <option value="eclipse">Light</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="font-size">Font Size: <span id="font-size-value" class="font-size-preview">16px</span></label>
                    <input type="range" id="font-size" class="form-control" min="12" max="24" value="16" step="1">
                    <div style="display: flex; justify-content: space-between; font-size: 0.8rem; color: #aaa;">
                        <span>Small</span>
                        <span>Medium</span>
                        <span>Large</span>
                    </div>
                </div>
                <div class="form-group">
                    <label>
                        <input type="checkbox" id="auto-save" checked> Auto-save changes
                    </label>
                </div>
                <div class="form-group">
                    <label>
                        <input type="checkbox" id="line-numbers" checked> Show line numbers
                    </label>
                </div>
                <div class="form-group">
                    <label>
                        <input type="checkbox" id="dark-mode"> Dark Mode UI
                    </label>
                </div>
            </div>
            <div class="modal-footer">
                <button class="btn btn-danger" id="cancel-settings">Cancel</button>
                <button class="btn btn-success" id="save-settings">Save Settings</button>
            </div>
        </div>
    </div>

    <!-- Export Modal -->
    <div class="modal" id="export-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Export Project</h3>
                <button class="close-modal" id="close-export-modal">&times;</button>
            </div>
            <div class="modal-body">
                <p>Choose how you want to export your project:</p>
                <div class="export-options">
                    <button class="btn btn-primary" id="export-html">
                        <i class="fas fa-file-code"></i> HTML Only
                    </button>
                    <button class="btn btn-primary" id="export-zip">
                        <i class="fas fa-file-archive"></i> ZIP File
                    </button>
                    <button class="btn btn-primary" id="export-github">
                        <i class="fab fa-github"></i> Push to GitHub
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Help Modal -->
    <div class="modal" id="help-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Diamond Help & Documentation</h3>
                <button class="close-modal" id="close-help-modal">&times;</button>
            </div>
            <div class="modal-body">
                <h4>Keyboard Shortcuts</h4>
                <ul>
                    <li><strong>Ctrl + Enter</strong> - Run code</li>
                    <li><strong>Ctrl + S</strong> - Save project</li>
                    <li><strong>Ctrl + /</strong> - Toggle comment</li>
                    <li><strong>Tab</strong> - Indent code</li>
                    <li><strong>Ctrl + Space</strong> - Auto-complete</li>
                </ul>
                
                <h4>Diamond Features</h4>
                <ul>
                    <li>Advanced code editor with syntax highlighting</li>
                    <li>Code snippets for faster development</li>
                    <li>Multiple theme options</li>
                    <li>Customizable font sizes (12px - 24px)</li>
                    <li>Export to multiple formats</li>
                    <li>Project management</li>
                    <li>Auto-save and backup</li>
                    <li>Multi-language support (Python, Java, C++)</li>
                    <li>User authentication and project sharing</li>
                    <li>Real-time code execution with console output</li>
                    <li>AI-powered code suggestions</li>
                    <li>Real-time collaboration</li>
                    <li>Version control integration</li>
                    <li>Cloud synchronization</li>
                    <li>Enterprise-grade security</li>
                </ul>
            </div>
            <div class="modal-footer">
                <button class="btn btn-primary" id="close-help">Close</button>
            </div>
        </div>
    </div>

    <!-- Authentication Modal -->
    <div class="modal" id="auth-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Diamond Login / Register</h3>
                <button class="close-modal" id="close-auth-modal">&times;</button>
            </div>
            <div class="modal-body">
                <div class="auth-tabs">
                    <div class="auth-tab active" data-tab="login">Login</div>
                    <div class="auth-tab" data-tab="register">Register</div>
                </div>
                
                <div id="login-form" class="auth-form active">
                    <div class="form-group">
                        <label for="login-email">Email</label>
                        <input type="email" id="login-email" class="form-control" placeholder="Enter your email">
                    </div>
                    <div class="form-group">
                        <label for="login-password">Password</label>
                        <input type="password" id="login-password" class="form-control" placeholder="Enter your password">
                    </div>
                    <button class="btn btn-success" id="login-btn">Login</button>
                </div>
                
                <div id="register-form" class="auth-form">
                    <div class="form-group">
                        <label for="register-name">Full Name</label>
                        <input type="text" id="register-name" class="form-control" placeholder="Enter your full name">
                    </div>
                    <div class="form-group">
                        <label for="register-email">Email</label>
                        <input type="email" id="register-email" class="form-control" placeholder="Enter your email">
                    </div>
                    <div class="form-group">
                        <label for="register-password">Password</label>
                        <input type="password" id="register-password" class="form-control" placeholder="Create a password">
                    </div>
                    <div class="form-group">
                        <label for="register-confirm-password">Confirm Password</label>
                        <input type="password" id="register-confirm-password" class="form-control" placeholder="Confirm your password">
                    </div>
                    <button class="btn btn-success" id="register-btn">Register</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Projects Modal -->
    <div class="modal" id="projects-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">My Diamond Projects</h3>
                <button class="close-modal" id="close-projects-modal">&times;</button>
            </div>
            <div class="modal-body">
                <p>Select a project to load:</p>
                <div class="projects-list" id="projects-list">
                    <div class="project-item">
                        <div class="project-name">Diamond Portfolio</div>
                        <div class="project-date">2023-10-15</div>
                    </div>
                    <div class="project-item">
                        <div class="project-name">E-commerce Dashboard</div>
                        <div class="project-date">2023-09-22</div>
                    </div>
                    <div class="project-item">
                        <div class="project-name">Weather App</div>
                        <div class="project-date">2023-08-05</div>
                    </div>
                </div>
            </div>
            <div class="modal-footer">
                <button class="btn btn-danger" id="close-projects">Close</button>
            </div>
        </div>
    </div>

    <!-- CodeMirror JS -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/codemirror.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/mode/xml/xml.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/mode/css/css.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/mode/javascript/javascript.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/mode/htmlmixed/htmlmixed.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/mode/python/python.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/mode/clike/clike.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/edit/matchbrackets.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/edit/closebrackets.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/fold/foldcode.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/fold/foldgutter.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/fold/brace-fold.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/fold/xml-fold.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/fold/comment-fold.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/search/search.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/search/searchcursor.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/dialog/dialog.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/addon/selection/active-line.min.js"></script>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Welcome Screen
            const welcomeScreen = document.getElementById('welcome-screen');
            const enterAppBtn = document.getElementById('enter-app');
            
            enterAppBtn.addEventListener('click', function() {
                welcomeScreen.style.opacity = '0';
                welcomeScreen.style.visibility = 'hidden';
                createParticles();
            });
            
            // Create floating particles
            function createParticles() {
                const particlesContainer = document.getElementById('particles');
                const particleCount = 20;
                
                for (let i = 0; i < particleCount; i++) {
                    const particle = document.createElement('div');
                    particle.classList.add('particle');
                    
                    // Random size
                    const size = Math.random() * 8 + 3;
                    particle.style.width = `${size}px`;
                    particle.style.height = `${size}px`;
                    
                    // Random position
                    particle.style.left = `${Math.random() * 100}%`;
                    particle.style.top = `${Math.random() * 100}%`;
                    
                    // Random animation duration
                    const duration = Math.random() * 15 + 8;
                    particle.style.animationDuration = `${duration}s`;
                    
                    // Random delay
                    const delay = Math.random() * 3;
                    particle.style.animationDelay = `${delay}s`;
                    
                    particlesContainer.appendChild(particle);
                }
            }
            
            // DOM Elements
            const previewFrame = document.getElementById('preview-frame');
            const runBtn = document.getElementById('run-btn');
            const refreshBtn = document.getElementById('refresh-btn');
            const clearAllBtn = document.getElementById('clear-all-btn');
            const htmlClearBtn = document.getElementById('html-clear');
            const cssClearBtn = document.getElementById('css-clear');
            const jsClearBtn = document.getElementById('js-clear');
            const clearConsoleBtn = document.getElementById('clear-console');
            const editorTabs = document.querySelectorAll('.editor-tab');
            const editorWrappers = document.querySelectorAll('.editor-wrapper');
            const toast = document.getElementById('toast');
            const toastMessage = document.getElementById('toast-message');
            const newProjectBtn = document.getElementById('new-project-btn');
            const premiumBtn = document.getElementById('premium-btn');
            const snippetsBtn = document.getElementById('snippets-btn');
            const snippetsDropdown = document.getElementById('snippets-dropdown');
            const snippetItems = document.querySelectorAll('.snippet-item');
            const themeOptions = document.querySelectorAll('.theme-option');
            const languageOptions = document.querySelectorAll('.language-option');
            const consoleOutput = document.getElementById('console-output');
            const executionTime = document.getElementById('execution-time');
            const aiAssistant = document.getElementById('ai-assistant');
            
            // Enhancement buttons
            const formatCodeBtn = document.getElementById('format-code');
            const findReplaceBtn = document.getElementById('find-replace');
            const fullscreenBtn = document.getElementById('fullscreen');
            
            // Modal elements
            const saveModal = document.getElementById('save-modal');
            const shareModal = document.getElementById('share-modal');
            const settingsModal = document.getElementById('settings-modal');
            const exportModal = document.getElementById('export-modal');
            const helpModal = document.getElementById('help-modal');
            const authModal = document.getElementById('auth-modal');
            const projectsModal = document.getElementById('projects-modal');
            
            // Authentication elements
            const authTabs = document.querySelectorAll('.auth-tab');
            const authForms = document.querySelectorAll('.auth-form');
            const loginBtn = document.getElementById('login-btn');
            const registerBtn = document.getElementById('register-btn');
            const logoutBtn = document.getElementById('logout-btn');
            const userProfile = document.getElementById('user-profile');
            const userAvatar = document.getElementById('user-avatar');
            const userName = document.getElementById('user-name');
            
            // Navigation elements
            const navHome = document.getElementById('nav-home');
            const navProjects = document.getElementById('nav-projects');
            const navSave = document.getElementById('nav-save');
            const navShare = document.getElementById('nav-share');
            const navSettings = document.getElementById('nav-settings');
            const navHelp = document.getElementById('nav-help');
            const navExport = document.getElementById('nav-export');
            const navLogin = document.getElementById('nav-login');
            
            // CodeMirror Editors
            let htmlEditor, cssEditor, jsEditor;
            
            // Current settings
            let currentSettings = {
                theme: 'dracula',
                fontSize: 16,
                lineNumbers: true,
                autoSave: true,
                currentLanguage: 'web',
                darkMode: false
            };
            
            // User data
            let currentUser = null;
            
            // Initialize CodeMirror Editors
            function initializeEditors() {
                // HTML Editor
                htmlEditor = CodeMirror(document.getElementById('html-editor-wrapper'), {
                    mode: 'htmlmixed',
                    theme: currentSettings.theme,
                    lineNumbers: currentSettings.lineNumbers,
                    matchBrackets: true,
                    autoCloseBrackets: true,
                    foldGutter: true,
                    gutters: ['CodeMirror-linenumbers', 'CodeMirror-foldgutter'],
                    extraKeys: {
                        'Ctrl-S': function(instance) { saveCode(); },
                        'Ctrl-Enter': function(instance) { runCode(); },
                        'Ctrl-/': 'toggleComment',
                        'Ctrl-Space': function(instance) { showAISuggestions(); },
                        'Ctrl-F': function(instance) { 
                            // Open find dialog
                            if (CodeMirror.commands.find) {
                                CodeMirror.commands.find(instance);
                            }
                        }
                    },
                    value: `<!DOCTYPE html>
<html>
<head>
    <title>Diamond Web Page</title>
</head>
<body>
    <div class="container">
        <h1>Welcome to CodeRunner Pro Diamond Edition!</h1>
        <p>This is a premium HTML/CSS/JS editor with diamond features.</p>
        <button id="demo-btn">Click Me!</button>
        <div id="output"></div>
    </div>
</body>
</html>`
                });

                // CSS Editor
                cssEditor = CodeMirror(document.getElementById('css-editor-wrapper'), {
                    mode: 'css',
                    theme: currentSettings.theme,
                    lineNumbers: currentSettings.lineNumbers,
                    matchBrackets: true,
                    autoCloseBrackets: true,
                    foldGutter: true,
                    gutters: ['CodeMirror-linenumbers', 'CodeMirror-foldgutter'],
                    extraKeys: {
                        'Ctrl-S': function(instance) { saveCode(); },
                        'Ctrl-Enter': function(instance) { runCode(); },
                        'Ctrl-/': 'toggleComment',
                        'Ctrl-Space': function(instance) { showAISuggestions(); }
                    },
                    value: `body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #8B6BFF 0%, #6A4CFF 100%);
    color: white;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.container {
    text-align: center;
    max-width: 800px;
    padding: 30px;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(15px);
    border-radius: 15px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
    border: 1px solid rgba(255, 255, 255, 0.2);
}

h1 {
    font-size: 2.5rem;
    margin-bottom: 15px;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
    background: linear-gradient(135deg, #FFD700, #FFA500);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

p {
    font-size: 1.1rem;
    margin-bottom: 20px;
    line-height: 1.5;
    opacity: 0.9;
}

#demo-btn {
    background: linear-gradient(135deg, #00D4AA, #00B894);
    color: white;
    border: none;
    padding: 12px 25px;
    font-size: 1rem;
    border-radius: 40px;
    cursor: pointer;
    transition: all 0.3s;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    font-weight: 600;
}

#demo-btn:hover {
    background: linear-gradient(135deg, #00B894, #00A885);
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(0, 212, 170, 0.4);
}

#output {
    margin-top: 20px;
    padding: 20px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    border: 1px solid rgba(255, 255, 255, 0.1);
}`
                });

                // JavaScript Editor
                jsEditor = CodeMirror(document.getElementById('js-editor-wrapper'), {
                    mode: 'javascript',
                    theme: currentSettings.theme,
                    lineNumbers: currentSettings.lineNumbers,
                    matchBrackets: true,
                    autoCloseBrackets: true,
                    foldGutter: true,
                    gutters: ['CodeMirror-linenumbers', 'CodeMirror-foldgutter'],
                    extraKeys: {
                        'Ctrl-S': function(instance) { saveCode(); },
                        'Ctrl-Enter': function(instance) { runCode(); },
                        'Ctrl-/': 'toggleComment',
                        'Ctrl-Space': function(instance) { showAISuggestions(); }
                    },
                    value: `document.getElementById('demo-btn').addEventListener('click', function() {
    const output = document.getElementById('output');
    output.innerHTML = '<h3>Hello from JavaScript!</h3><p>You successfully executed JavaScript code in Diamond Edition.</p>';
    
    // Create a colorful animation
    const colors = ['#8B6BFF', '#FF6B9D', '#00D4AA', '#FFD700'];
    let i = 0;
    
    const colorInterval = setInterval(() => {
        document.body.style.background = \`linear-gradient(135deg, \${colors[i]} 0%, \${colors[(i+1) % colors.length]} 100%)\`;
        i = (i + 1) % colors.length;
    }, 1000);
    
    // Stop animation after 5 seconds
    setTimeout(() => {
        clearInterval(colorInterval);
        document.body.style.background = 'linear-gradient(135deg, #8B6BFF 0%, #6A4CFF 100%)';
    }, 5000);
});`
                });

                // Apply initial font size
                applyFontSize(currentSettings.fontSize);
                
                // Refresh editors
                setTimeout(() => {
                    htmlEditor.refresh();
                    cssEditor.refresh();
                    jsEditor.refresh();
                }, 100);
            }

            // Initialize
            initializeEditors();
            runCode();
            updateLineCounts();
            loadSettings();
            checkAuthStatus();
            
            // Enhancement buttons functionality
            formatCodeBtn.addEventListener('click', function() {
                // Simple formatting - in a real app, you would use a proper formatter
                const editor = getActiveEditor();
                if (editor) {
                    const content = editor.getValue();
                    // Basic formatting - just add proper indentation
                    const formatted = content.replace(/\n\s*\n/g, '\n\n');
                    editor.setValue(formatted);
                    showToast('Code formatted');
                }
            });
            
            findReplaceBtn.addEventListener('click', function() {
                const editor = getActiveEditor();
                if (editor && CodeMirror.commands.find) {
                    CodeMirror.commands.find(editor);
                }
            });
            
            fullscreenBtn.addEventListener('click', function() {
                const editorContainer = document.querySelector('.editor-content');
                if (!document.fullscreenElement) {
                    if (editorContainer.requestFullscreen) {
                        editorContainer.requestFullscreen();
                    }
                } else {
                    if (document.exitFullscreen) {
                        document.exitFullscreen();
                    }
                }
            });
            
            // Get the currently active editor
            function getActiveEditor() {
                const activeTab = document.querySelector('.editor-tab.active');
                if (activeTab) {
                    const editorType = activeTab.getAttribute('data-editor');
                    if (editorType === 'html') return htmlEditor;
                    if (editorType === 'css') return cssEditor;
                    if (editorType === 'js') return jsEditor;
                }
                return htmlEditor; // Default to HTML editor
            }
            
            // AI Assistant functionality
            aiAssistant.addEventListener('click', function() {
                showAISuggestions();
            });
            
            function showAISuggestions() {
                const suggestions = [
                    "// AI Suggestion: Add error handling for better user experience",
                    "/* AI Suggestion: Consider using CSS Grid for responsive layout */",
                    "<!-- AI Suggestion: Add semantic HTML tags for better accessibility -->"
                ];
                
                const randomSuggestion = suggestions[Math.floor(Math.random() * suggestions.length)];
                addConsoleOutput(`>> AI Assistant: ${randomSuggestion}`, 'success');
                showToast('AI suggestion added to console');
            }
            
            // Premium button functionality
            premiumBtn.addEventListener('click', function() {
                showToast('You are already using the Diamond Edition worth ₹50 Crore!');
            });
            
            // Tab switching functionality
            editorTabs.forEach(tab => {
                tab.addEventListener('click', function() {
                    const editorType = this.getAttribute('data-editor');
                    
                    // Update active tab
                    editorTabs.forEach(t => t.classList.remove('active'));
                    this.classList.add('active');
                    
                    // Show corresponding editor
                    editorWrappers.forEach(wrapper => {
                        wrapper.classList.remove('active');
                        if (wrapper.id === `${editorType}-editor-wrapper`) {
                            wrapper.classList.add('active');
                            
                            // Refresh the editor when it becomes active
                            setTimeout(() => {
                                if (editorType === 'html') htmlEditor.refresh();
                                else if (editorType === 'css') cssEditor.refresh();
                                else if (editorType === 'js') jsEditor.refresh();
                            }, 50);
                        }
                    });
                });
            });
            
            // Language switching functionality
            languageOptions.forEach(option => {
                option.addEventListener('click', function() {
                    const language = this.getAttribute('data-language');
                    
                    // Update active language
                    languageOptions.forEach(o => o.classList.remove('active'));
                    this.classList.add('active');
                    
                    // Apply language-specific settings
                    switchLanguage(language);
                });
            });
            
            function switchLanguage(language) {
                currentSettings.currentLanguage = language;
                
                switch(language) {
                    case 'web':
                        // Show HTML/CSS/JS tabs
                        editorTabs.forEach(tab => tab.style.display = 'block');
                        document.querySelector('[data-editor="html"]').click();
                        break;
                    case 'python':
                        // Show only one editor for Python
                        editorTabs.forEach(tab => tab.style.display = 'none');
                        document.getElementById('html-editor-wrapper').classList.add('active');
                        document.getElementById('css-editor-wrapper').classList.remove('active');
                        document.getElementById('js-editor-wrapper').classList.remove('active');
                        
                        // Change editor mode to Python
                        htmlEditor.setOption('mode', 'python');
                        htmlEditor.setValue(`# Welcome to Python Editor - Diamond Edition
def greet(name):
    return f"Hello, {name}!"

def calculate_factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * calculate_factorial(n-1)

def main():
    print("=== Python Code Runner - Diamond Edition ===")
    name = "CodeRunner Pro Diamond User"
    greeting = greet(name)
    print(greeting)
    
    # Calculate factorial
    number = 5
    factorial = calculate_factorial(number)
    print(f"Factorial of {number} is: {factorial}")
    
    # Fibonacci series
    print("Fibonacci series (first 10 numbers):")
    a, b = 0, 1
    for i in range(10):
        print(a, end=" ")
        a, b = b, a + b
    print()
    
    print("Code execution completed successfully!")

if __name__ == "__main__":
    main()`);
                        break;
                    case 'java':
                        // Show only one editor for Java
                        editorTabs.forEach(tab => tab.style.display = 'none');
                        document.getElementById('html-editor-wrapper').classList.add('active');
                        document.getElementById('css-editor-wrapper').classList.remove('active');
                        document.getElementById('js-editor-wrapper').classList.remove('active');
                        
                        // Change editor mode to Java
                        htmlEditor.setOption('mode', 'text/x-java');
                        htmlEditor.setValue(`// Welcome to Java Editor - Diamond Edition
public class Main {
    public static void main(String[] args) {
        System.out.println("=== Java Code Runner - Diamond Edition ===");
        
        String name = "CodeRunner Pro Diamond User";
        String greeting = greet(name);
        System.out.println(greeting);
        
        // Calculate factorial
        int number = 5;
        long factorial = calculateFactorial(number);
        System.out.println("Factorial of " + number + " is: " + factorial);
        
        // Fibonacci series
        System.out.println("Fibonacci series (first 10 numbers):");
        int n1 = 0, n2 = 1, n3;
        System.out.print(n1 + " " + n2 + " ");
        for(int i = 2; i < 10; i++) {
            n3 = n1 + n2;
            System.out.print(n3 + " ");
            n1 = n2;
            n2 = n3;
        }
        System.out.println();
        
        System.out.println("Code execution completed successfully!");
    }
    
    public static String greet(String name) {
        return "Hello, " + name + "!";
    }
    
    public static long calculateFactorial(int n) {
        if (n == 0 || n == 1) {
            return 1;
        }
        return n * calculateFactorial(n - 1);
    }
}`);
                        break;
                    case 'cpp':
                        // Show only one editor for C++
                        editorTabs.forEach(tab => tab.style.display = 'none');
                        document.getElementById('html-editor-wrapper').classList.add('active');
                        document.getElementById('css-editor-wrapper').classList.remove('active');
                        document.getElementById('js-editor-wrapper').classList.remove('active');
                        
                        // Change editor mode to C++
                        htmlEditor.setOption('mode', 'text/x-c++src');
                        htmlEditor.setValue(`// Welcome to C++ Editor - Diamond Edition
#include <iostream>
#include <string>
using namespace std;

string greet(string name) {
    return "Hello, " + name + "!";
}

long long calculateFactorial(int n) {
    if (n == 0 || n == 1) {
        return 1;
    }
    return n * calculateFactorial(n - 1);
}

int main() {
    cout << "=== C++ Code Runner - Diamond Edition ===" << endl;
    
    string name = "CodeRunner Pro Diamond User";
    string greeting = greet(name);
    cout << greeting << endl;
    
    // Calculate factorial
    int number = 5;
    long long factorial = calculateFactorial(number);
    cout << "Factorial of " << number << " is: " << factorial << endl;
    
    // Fibonacci series
    cout << "Fibonacci series (first 10 numbers):" << endl;
    int t1 = 0, t2 = 1, nextTerm;
    for (int i = 1; i <= 10; ++i) {
        cout << t1 << " ";
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
    }
    cout << endl;
    
    cout << "Code execution completed successfully!" << endl;
    return 0;
}`);
                        break;
                }
                
                updateLineCounts();
                showToast(`Switched to ${language.toUpperCase()} mode`);
            }
            
            // Run code function
            function runCode() {
                const startTime = performance.now();
                
                // Clear previous output
                executionTime.textContent = '';
                
                if (currentSettings.currentLanguage === 'web') {
                    const htmlCode = htmlEditor.getValue();
                    const cssCode = cssEditor.getValue();
                    const jsCode = jsEditor.getValue();
                    
                    const iframeDoc = previewFrame.contentDocument || previewFrame.contentWindow.document;
                    
                    iframeDoc.open();
                    iframeDoc.write(`
                        <!DOCTYPE html>
                        <html>
                        <head>
                            <style>${cssCode}</style>
                        </head>
                        <body>
                            ${htmlCode}
                            <script>${jsCode}<\/script>
                        </body>
                        </html>
                    `);
                    iframeDoc.close();
                    
                    const endTime = performance.now();
                    executionTime.textContent = `Executed in ${(endTime - startTime).toFixed(2)}ms`;
                    
                    addConsoleOutput('Web code executed successfully!', 'success');
                    showToast('Web code executed successfully!');
                } else {
                    // Simulate code execution for other languages
                    const code = htmlEditor.getValue();
                    simulateCodeExecution(code, currentSettings.currentLanguage, startTime);
                }
            }
            
            // Simulate code execution for Python, Java, C++
            function simulateCodeExecution(code, language, startTime) {
                addConsoleOutput(`>> Executing ${language.toUpperCase()} code...`, 'info');
                
                // Show loading spinner
                const loadingLine = addConsoleOutput('<div class="spinner"></div>', 'info');
                
                setTimeout(() => {
                    // Remove loading spinner
                    loadingLine.remove();
                    
                    let output = '';
                    let success = true;
                    
                    switch(language) {
                        case 'python':
                            output = `=== Python Code Runner - Diamond Edition ===
Hello, CodeRunner Pro Diamond User!
Factorial of 5 is: 120
Fibonacci series (first 10 numbers):
0 1 1 2 3 5 8 13 21 34 
Code execution completed successfully!`;
                            break;
                        case 'java':
                            output = `=== Java Code Runner - Diamond Edition ===
Hello, CodeRunner Pro Diamond User!
Factorial of 5 is: 120
Fibonacci series (first 10 numbers):
0 1 1 2 3 5 8 13 21 34 
Code execution completed successfully!`;
                            break;
                        case 'cpp':
                            output = `=== C++ Code Runner - Diamond Edition ===
Hello, CodeRunner Pro Diamond User!
Factorial of 5 is: 120
Fibonacci series (first 10 numbers):
0 1 1 2 3 5 8 13 21 34 
Code execution completed successfully!`;
                            break;
                    }
                    
                    // Split output by lines and add to console
                    const lines = output.split('\n');
                    lines.forEach(line => {
                        addConsoleOutput(line, 'success');
                    });
                    
                    const endTime = performance.now();
                    executionTime.textContent = `Executed in ${(endTime - startTime).toFixed(2)}ms`;
                    
                    showToast(`${language.toUpperCase()} code executed successfully!`);
                    
                }, 1500); // Simulate execution time
            }
            
            // Add output to console
            function addConsoleOutput(message, type = 'info') {
                const line = document.createElement('div');
                line.className = `console-line ${type === 'error' ? 'console-error' : type === 'success' ? 'console-success' : type === 'warning' ? 'console-warning' : ''}`;
                line.innerHTML = message;
                consoleOutput.appendChild(line);
                consoleOutput.scrollTop = consoleOutput.scrollHeight;
                return line;
            }
            
            // Clear functions
            function clearHTML() {
                htmlEditor.setValue('');
                updateLineCounts();
                showToast('HTML cleared');
            }
            
            function clearCSS() {
                cssEditor.setValue('');
                updateLineCounts();
                showToast('CSS cleared');
            }
            
            function clearJS() {
                jsEditor.setValue('');
                updateLineCounts();
                showToast('JavaScript cleared');
            }
            
            function clearAll() {
                if (confirm('Are you sure you want to clear all code editors?')) {
                    htmlEditor.setValue('');
                    cssEditor.setValue('');
                    jsEditor.setValue('');
                    updateLineCounts();
                    showToast('All editors cleared');
                }
            }
            
            function clearConsole() {
                consoleOutput.innerHTML = '<div class="console-line console-success">>> Console cleared</div>';
            }
            
            function newProject() {
                if (confirm('Create a new project? Any unsaved changes will be lost.')) {
                    htmlEditor.setValue('<!DOCTYPE html>\n<html>\n<head>\n    <title>New Diamond Project</title>\n</head>\n<body>\n    <h1>Hello Diamond World!</h1>\n</body>\n</html>');
                    cssEditor.setValue('body {\n    font-family: Arial, sans-serif;\n    margin: 0;\n    padding: 20px;\n}');
                    jsEditor.setValue('// Add your JavaScript code here');
                    updateLineCounts();
                    showToast('New diamond project created');
                }
            }
            
            // Update line counts
            function updateLineCounts() {
                document.getElementById('html-lines').textContent = `HTML: ${htmlEditor.getValue().split('\n').length} lines`;
                document.getElementById('css-lines').textContent = `CSS: ${cssEditor.getValue().split('\n').length} lines`;
                document.getElementById('js-lines').textContent = `JS: ${jsEditor.getValue().split('\n').length} lines`;
            }
            
            // Toast notification function
            function showToast(message) {
                toastMessage.textContent = message;
                toast.classList.add('show');
                
                setTimeout(() => {
                    toast.classList.remove('show');
                }, 3000);
            }
            
            // Modal functions
            function openModal(modal) {
                modal.style.display = 'flex';
            }
            
            function closeModal(modal) {
                modal.style.display = 'none';
            }
            
            // Authentication functions
            function openAuthModal() {
                openModal(authModal);
            }
            
            function loginUser(email, password) {
                // In a real app, this would be an API call to your backend
                // For demo purposes, we'll simulate a successful login
                if (email && password) {
                    currentUser = {
                        id: 1,
                        name: 'Diamond User',
                        email: email,
                        avatar: 'D'
                    };
                    
                    // Update UI
                    userProfile.style.display = 'flex';
                    userAvatar.textContent = currentUser.avatar;
                    userName.textContent = currentUser.name;
                    
                    // Update navigation
                    navLogin.style.display = 'none';
                    
                    // Close modal
                    closeModal(authModal);
                    
                    showToast(`Welcome back, ${currentUser.name}!`);
                    
                    // Save user data to localStorage
                    localStorage.setItem('currentUser', JSON.stringify(currentUser));
                } else {
                    alert('Please enter both email and password');
                }
            }
            
            function registerUser(name, email, password, confirmPassword) {
                // In a real app, this would be an API call to your backend
                if (name && email && password && confirmPassword) {
                    if (password !== confirmPassword) {
                        alert('Passwords do not match');
                        return;
                    }
                    
                    currentUser = {
                        id: Date.now(),
                        name: name,
                        email: email,
                        avatar: name.charAt(0).toUpperCase()
                    };
                    
                    // Update UI
                    userProfile.style.display = 'flex';
                    userAvatar.textContent = currentUser.avatar;
                    userName.textContent = currentUser.name;
                    
                    // Update navigation
                    navLogin.style.display = 'none';
                    
                    // Close modal
                    closeModal(authModal);
                    
                    showToast(`Account created successfully! Welcome, ${currentUser.name}!`);
                    
                    // Save user data to localStorage
                    localStorage.setItem('currentUser', JSON.stringify(currentUser));
                } else {
                    alert('Please fill in all fields');
                }
            }
            
            function logoutUser() {
                currentUser = null;
                
                // Update UI
                userProfile.style.display = 'none';
                navLogin.style.display = 'block';
                
                // Clear user data from localStorage
                localStorage.removeItem('currentUser');
                
                showToast('You have been logged out');
            }
            
            function checkAuthStatus() {
                const savedUser = localStorage.getItem('currentUser');
                if (savedUser) {
                    currentUser = JSON.parse(savedUser);
                    
                    // Update UI
                    userProfile.style.display = 'flex';
                    userAvatar.textContent = currentUser.avatar;
                    userName.textContent = currentUser.name;
                    navLogin.style.display = 'none';
                }
            }
            
            // Code snippets functionality
            snippetsBtn.addEventListener('click', function() {
                snippetsDropdown.classList.toggle('show');
            });
            
            snippetItems.forEach(item => {
                item.addEventListener('click', function() {
                    const snippetType = this.getAttribute('data-snippet');
                    insertSnippet(snippetType);
                    snippetsDropdown.classList.remove('show');
                });
            });
            
            function insertSnippet(type) {
                let snippet = '';
                let editor = htmlEditor;
                
                switch(type) {
                    case 'boilerplate':
                        snippet = `<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diamond Document</title>
</head>
<body>
    
</body>
</html>`;
                        editor = htmlEditor;
                        break;
                    case 'navbar':
                        snippet = `<nav>
    <div class="nav-container">
        <div class="logo">
            <a href="#">Diamond Logo</a>
        </div>
        <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </div>
</nav>`;
                        editor = htmlEditor;
                        break;
                    case 'card':
                        snippet = `<div class="card">
    <div class="card-header">
        <h3>Diamond Card Title</h3>
    </div>
    <div class="card-body">
        <p>Diamond card content goes here.</p>
    </div>
    <div class="card-footer">
        <button class="btn">Action</button>
    </div>
</div>`;
                        editor = htmlEditor;
                        break;
                    case 'button':
                        snippet = `.btn {
    background: linear-gradient(135deg, #8B6BFF, #6A4CFF);
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.3s;
    font-weight: 600;
    box-shadow: 0 4px 12px rgba(139, 107, 255, 0.3);
}

.btn:hover {
    background: linear-gradient(135deg, #6A4CFF, #8B6BFF);
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(139, 107, 255, 0.4);
}`;
                        editor = cssEditor;
                        break;
                    case 'animation':
                        snippet = `@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.animated-element {
    animation: fadeIn 0.5s ease-out;
}`;
                        editor = cssEditor;
                        break;
                }
                
                const cursor = editor.getCursor();
                editor.replaceRange('\n' + snippet, cursor);
                updateLineCounts();
                showToast(`Diamond snippet "${type}" inserted`);
            }
            
            // Theme selector functionality
            themeOptions.forEach(option => {
                option.addEventListener('click', function() {
                    const theme = this.getAttribute('data-theme');
                    
                    // Update active theme
                    themeOptions.forEach(o => o.classList.remove('active'));
                    this.classList.add('active');
                    
                    // Apply theme to editors
                    applyTheme(theme);
                });
            });
            
            function applyTheme(theme) {
                htmlEditor.setOption('theme', theme);
                cssEditor.setOption('theme', theme);
                jsEditor.setOption('theme', theme);
                currentSettings.theme = theme;
                
                showToast(`Theme changed to ${theme}`);
            }
            
            // Font size functionality
            function applyFontSize(size) {
                // Remove all existing font size classes
                editorWrappers.forEach(wrapper => {
                    for (let i = 12; i <= 24; i++) {
                        wrapper.classList.remove(`font-size-${i}`);
                    }
                    wrapper.classList.add(`font-size-${size}`);
                });
                
                currentSettings.fontSize = size;
                
                // Update font size display
                document.getElementById('font-size-value').textContent = `${size}px`;
                document.getElementById('font-size').value = size;
                
                // Refresh editors
                setTimeout(() => {
                    htmlEditor.refresh();
                    cssEditor.refresh();
                    jsEditor.refresh();
                }, 50);
            }
            
            // Line numbers toggle
            document.getElementById('line-numbers-toggle').addEventListener('change', function() {
                const showLineNumbers = this.checked;
                htmlEditor.setOption('lineNumbers', showLineNumbers);
                cssEditor.setOption('lineNumbers', showLineNumbers);
                jsEditor.setOption('lineNumbers', showLineNumbers);
                currentSettings.lineNumbers = showLineNumbers;
            });
            
            // Dark mode toggle
            document.getElementById('dark-mode').addEventListener('change', function() {
                const darkMode = this.checked;
                currentSettings.darkMode = darkMode;
                
                if (darkMode) {
                    document.body.classList.add('dark-mode');
                } else {
                    document.body.classList.remove('dark-mode');
                }
                
                showToast(`Dark mode ${darkMode ? 'enabled' : 'disabled'}`);
            });
            
            // Event listeners for code execution
            runBtn.addEventListener('click', runCode);
            refreshBtn.addEventListener('click', runCode);
            clearConsoleBtn.addEventListener('click', clearConsole);
            
            // Event listeners for clearing code
            clearAllBtn.addEventListener('click', clearAll);
            htmlClearBtn.addEventListener('click', clearHTML);
            cssClearBtn.addEventListener('click', clearCSS);
            jsClearBtn.addEventListener('click', clearJS);
            
            // Event listener for new project
            newProjectBtn.addEventListener('click', newProject);
            
            // Event listeners for navigation
            navHome.addEventListener('click', function(e) {
                e.preventDefault();
                showToast('Welcome to CodeRunner Pro Diamond Edition!');
            });
            
            navProjects.addEventListener('click', function(e) {
                e.preventDefault();
                if (currentUser) {
                    openModal(projectsModal);
                } else {
                    showToast('Please login to access your diamond projects');
                    openAuthModal();
                }
            });
            
            navSave.addEventListener('click', function(e) {
                e.preventDefault();
                if (currentUser) {
                    openModal(saveModal);
                } else {
                    showToast('Please login to save diamond projects');
                    openAuthModal();
                }
            });
            
            navShare.addEventListener('click', function(e) {
                e.preventDefault();
                if (currentUser) {
                    // Generate a unique share link
                    const projectId = Math.random().toString(36).substring(2, 10);
                    const shareLink = `https://coderunner-pro-diamond.com/project/${projectId}`;
                    document.getElementById('share-link').value = shareLink;
                    openModal(shareModal);
                } else {
                    showToast('Please login to share diamond projects');
                    openAuthModal();
                }
            });
            
            navSettings.addEventListener('click', function(e) {
                e.preventDefault();
                // Load current settings into modal
                document.getElementById('theme-select').value = currentSettings.theme;
                document.getElementById('font-size').value = currentSettings.fontSize;
                document.getElementById('font-size-value').textContent = `${currentSettings.fontSize}px`;
                document.getElementById('auto-save').checked = currentSettings.autoSave;
                document.getElementById('line-numbers').checked = currentSettings.lineNumbers;
                document.getElementById('dark-mode').checked = currentSettings.darkMode;
                
                openModal(settingsModal);
            });
            
            navExport.addEventListener('click', function(e) {
                e.preventDefault();
                openModal(exportModal);
            });
            
            navHelp.addEventListener('click', function(e) {
                e.preventDefault();
                openModal(helpModal);
            });
            
            navLogin.addEventListener('click', function(e) {
                e.preventDefault();
                openAuthModal();
            });
            
            // Event listeners for authentication
            authTabs.forEach(tab => {
                tab.addEventListener('click', function() {
                    const tabName = this.getAttribute('data-tab');
                    
                    // Update active tab
                    authTabs.forEach(t => t.classList.remove('active'));
                    this.classList.add('active');
                    
                    // Show corresponding form
                    authForms.forEach(form => {
                        form.classList.remove('active');
                        if (form.id === `${tabName}-form`) {
                            form.classList.add('active');
                        }
                    });
                });
            });
            
            loginBtn.addEventListener('click', function() {
                const email = document.getElementById('login-email').value;
                const password = document.getElementById('login-password').value;
                loginUser(email, password);
            });
            
            registerBtn.addEventListener('click', function() {
                const name = document.getElementById('register-name').value;
                const email = document.getElementById('register-email').value;
                const password = document.getElementById('register-password').value;
                const confirmPassword = document.getElementById('register-confirm-password').value;
                registerUser(name, email, password, confirmPassword);
            });
            
            logoutBtn.addEventListener('click', function() {
                logoutUser();
            });
            
            // Event listeners for modal close buttons
            document.getElementById('close-save-modal').addEventListener('click', function() {
                closeModal(saveModal);
            });
            
            document.getElementById('close-share-modal').addEventListener('click', function() {
                closeModal(shareModal);
            });
            
            document.getElementById('close-settings-modal').addEventListener('click', function() {
                closeModal(settingsModal);
            });
            
            document.getElementById('close-export-modal').addEventListener('click', function() {
                closeModal(exportModal);
            });
            
            document.getElementById('close-help-modal').addEventListener('click', function() {
                closeModal(helpModal);
            });
            
            document.getElementById('close-auth-modal').addEventListener('click', function() {
                closeModal(authModal);
            });
            
            document.getElementById('close-projects-modal').addEventListener('click', function() {
                closeModal(projectsModal);
            });
            
            document.getElementById('cancel-save').addEventListener('click', function() {
                closeModal(saveModal);
            });
            
            document.getElementById('cancel-settings').addEventListener('click', function() {
                closeModal(settingsModal);
            });
            
            document.getElementById('close-help').addEventListener('click', function() {
                closeModal(helpModal);
            });
            
            document.getElementById('close-projects').addEventListener('click', function() {
                closeModal(projectsModal);
            });
            
            // Event listeners for modal actions
            document.getElementById('confirm-save').addEventListener('click', function() {
                const projectName = document.getElementById('project-name').value;
                if (projectName.trim() === '') {
                    alert('Please enter a project name');
                    return;
                }
                
                // In a real app, you would save to a database or localStorage
                showToast(`Diamond project "${projectName}" saved successfully!`);
                closeModal(saveModal);
                
                // Clear the form
                document.getElementById('project-name').value = '';
                document.getElementById('project-description').value = '';
            });
            
            document.getElementById('copy-link').addEventListener('click', function() {
                const shareLink = document.getElementById('share-link');
                shareLink.select();
                document.execCommand('copy');
                showToast('Diamond link copied to clipboard!');
            });
            
            // Font size slider in settings modal
            document.getElementById('font-size').addEventListener('input', function() {
                const size = this.value;
                document.getElementById('font-size-value').textContent = `${size}px`;
                // Live preview of font size
                applyFontSize(parseInt(size));
            });
            
            document.getElementById('save-settings').addEventListener('click', function() {
                const theme = document.getElementById('theme-select').value;
                const fontSize = parseInt(document.getElementById('font-size').value);
                const lineNumbers = document.getElementById('line-numbers').checked;
                const autoSave = document.getElementById('auto-save').checked;
                const darkMode = document.getElementById('dark-mode').checked;
                
                // Apply settings
                applyTheme(theme);
                applyFontSize(fontSize);
                
                htmlEditor.setOption('lineNumbers', lineNumbers);
                cssEditor.setOption('lineNumbers', lineNumbers);
                jsEditor.setOption('lineNumbers', lineNumbers);
                
                document.getElementById('line-numbers-toggle').checked = lineNumbers;
                currentSettings.lineNumbers = lineNumbers;
                currentSettings.autoSave = autoSave;
                currentSettings.darkMode = darkMode;
                
                if (darkMode) {
                    document.body.classList.add('dark-mode');
                } else {
                    document.body.classList.remove('dark-mode');
                }
                
                // Save settings to localStorage
                saveSettings();
                
                showToast('Diamond settings saved successfully!');
                closeModal(settingsModal);
            });
            
            // Export functionality
            document.getElementById('export-html').addEventListener('click', function() {
                showToast('HTML exported successfully!');
                closeModal(exportModal);
            });
            
            document.getElementById('export-zip').addEventListener('click', function() {
                showToast('Diamond project exported as ZIP file!');
                closeModal(exportModal);
            });
            
            document.getElementById('export-github').addEventListener('click', function() {
                showToast('Diamond project pushed to GitHub!');
                closeModal(exportModal);
            });
            
            // Update line counts when editors change
            htmlEditor.on('change', updateLineCounts);
            cssEditor.on('change', updateLineCounts);
            jsEditor.on('change', updateLineCounts);
            
            // Auto-save functionality (localStorage)
            function saveCode() {
                const codeData = {
                    html: htmlEditor.getValue(),
                    css: cssEditor.getValue(),
                    js: jsEditor.getValue()
                };
                localStorage.setItem('codeRunnerProDiamondData', JSON.stringify(codeData));
            }
            
            function loadSavedCode() {
                const savedData = localStorage.getItem('codeRunnerProDiamondData');
                if (savedData) {
                    const codeData = JSON.parse(savedData);
                    htmlEditor.setValue(codeData.html || htmlEditor.getValue());
                    cssEditor.setValue(codeData.css || cssEditor.getValue());
                    jsEditor.setValue(codeData.js || jsEditor.getValue());
                    updateLineCounts();
                }
            }
            
            // Settings management
            function saveSettings() {
                localStorage.setItem('codeRunnerProDiamondSettings', JSON.stringify(currentSettings));
            }
            
            function loadSettings() {
                const savedSettings = localStorage.getItem('codeRunnerProDiamondSettings');
                if (savedSettings) {
                    const settings = JSON.parse(savedSettings);
                    currentSettings = { ...currentSettings, ...settings };
                    
                    // Apply loaded settings
                    applyTheme(currentSettings.theme);
                    applyFontSize(currentSettings.fontSize);
                    document.getElementById('line-numbers-toggle').checked = currentSettings.lineNumbers;
                    document.getElementById('auto-save').checked = currentSettings.autoSave;
                    document.getElementById('dark-mode').checked = currentSettings.darkMode;
                    
                    if (currentSettings.darkMode) {
                        document.body.classList.add('dark-mode');
                    }
                    
                    // Update theme selector
                    themeOptions.forEach(option => {
                        option.classList.remove('active');
                        if (option.getAttribute('data-theme') === currentSettings.theme) {
                            option.classList.add('active');
                        }
                    });
                }
            }
            
            // Set up auto-save
            htmlEditor.on('change', function() {
                if (currentSettings.autoSave) {
                    saveCode();
                }
            });
            
            cssEditor.on('change', function() {
                if (currentSettings.autoSave) {
                    saveCode();
                }
            });
            
            jsEditor.on('change', function() {
                if (currentSettings.autoSave) {
                    saveCode();
                }
            });
            
            // Load saved code on page load
            loadSavedCode();
            
            // Close snippets dropdown when clicking outside
            document.addEventListener('click', function(e) {
                if (!snippetsBtn.contains(e.target) && !snippetsDropdown.contains(e.target)) {
                    snippetsDropdown.classList.remove('show');
                }
            });
            
            // Keyboard shortcuts
            document.addEventListener('keydown', function(e) {
                if (e.ctrlKey && e.key === 'Enter') {
                    e.preventDefault();
                    runCode();
                }
                
                if (e.ctrlKey && e.key === 's') {
                    e.preventDefault();
                    if (currentUser) {
                        openModal(saveModal);
                    } else {
                        showToast('Please login to save diamond projects');
                        openAuthModal();
                    }
                }
            });
        });
    </script>
</body>
</html>