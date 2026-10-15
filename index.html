<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shadow AI // Advanced Neural Assistant</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Google+Sans:wght@400;500;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root {
    --bg-main: #131314;
    --bg-sidebar: #1e1f20;
    --bg-surface: #1e1f20;
    --bg-surface-hover: #282a2c;
    --bg-input: #1e1f20;
    --text-primary: #e3e3e3;
    --text-secondary: #c4c7c5;
    --text-muted: #8e918f;
    --border-subtle: #2d2f31;
    --gemini-blue: #4285f4;
    --gemini-purple: #9b72cb;
    --gemini-pink: #d96570;
    --accent-glow: #1a73e8;
    --alert-red: #ea4335;
    --success-green: #34a853;
    --font-sans: 'Google Sans', 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
}

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
    min-height: 100vh;
    background-color: var(--bg-main);
    color: var(--text-primary);
    font-family: var(--font-sans);
    display: flex;
    overflow: hidden;
    position: relative;
}

/* AMBIENT AURORA DRIFT ANIMATION */
body::before {
    content: '';
    position: fixed;
    top: -20%;
    left: 15%;
    width: 70vw;
    height: 70vh;
    background: radial-gradient(circle, rgba(66, 133, 244, 0.08) 0%, rgba(155, 114, 203, 0.05) 45%, rgba(217, 101, 112, 0.03) 70%, transparent 85%);
    filter: blur(90px);
    pointer-events: none;
    z-index: 0;
    animation: auroraDrift 16s ease-in-out infinite alternate;
}

@keyframes auroraDrift {
    0% { transform: translate(0, 0) scale(1); }
    50% { transform: translate(-8%, 12%) scale(1.12); }
    100% { transform: translate(8%, -8%) scale(1.05); }
}

/* AUTHENTICATION OVERLAY */
#loginScreen {
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    background: #131314;
    z-index: 10000;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    transition: opacity 0.4s cubic-bezier(0.16, 1, 0.3, 1);
}

.gemini-auth-card {
    background: #1e1f20;
    border: 1px solid #333538;
    border-radius: 28px;
    padding: 44px 36px;
    width: 100%;
    max-width: 420px;
    text-align: center;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6);
    animation: modalPopIn 0.35s cubic-bezier(0.16, 1, 0.3, 1) forwards;
    position: relative;
}

.gemini-sparkle-logo {
    width: 52px;
    height: 52px;
    margin: 0 auto 16px;
    background: linear-gradient(135deg, #4285f4, #9b72cb, #d96570);
    border-radius: 16px;
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 0 0 25px rgba(155, 114, 203, 0.4);
    cursor: pointer;
    transition: transform 0.4s ease, box-shadow 0.4s ease;
}

.gemini-sparkle-logo:hover {
    transform: rotate(12deg) scale(1.08);
    box-shadow: 0 0 35px rgba(217, 101, 112, 0.6);
}

.gemini-sparkle-logo svg { width: 30px; height: 30px; fill: #ffffff; transition: transform 0.4s ease; }
.gemini-sparkle-logo:hover svg { transform: scale(1.1); }

.auth-title { font-size: 24px; font-weight: 700; color: #fff; margin-bottom: 6px; letter-spacing: -0.5px; }
.auth-sub { font-size: 13px; color: var(--text-secondary); margin-bottom: 26px; }

.auth-input-group { margin-bottom: 14px; text-align: left; position: relative; }
.auth-input-group label { font-size: 12px; color: var(--text-secondary); font-weight: 500; display: block; margin-bottom: 6px; }

.auth-input {
    width: 100%;
    background: #131314;
    border: 1px solid #3c4043;
    border-radius: 12px;
    padding: 12px 14px;
    color: #fff;
    font-size: 14px;
    outline: none;
    transition: all 0.2s;
}

.auth-input:focus { border-color: #a8c7fa; box-shadow: 0 0 0 2px rgba(168, 199, 250, 0.2); }

.toggle-pass-btn {
    position: absolute;
    right: 12px;
    bottom: 11px;
    background: none;
    border: none;
    color: var(--text-muted);
    cursor: pointer;
    font-size: 16px;
}

.auth-btn {
    width: 100%;
    background: linear-gradient(90deg, #1a73e8, #8ab4f8);
    color: #0b1528;
    border: none;
    padding: 13px;
    border-radius: 20px;
    font-size: 14px;
    font-weight: 700;
    cursor: pointer;
    margin-top: 10px;
    transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}
.auth-btn:hover {
    opacity: 0.95;
    transform: translateY(-1px);
    box-shadow: 0 4px 15px rgba(26, 115, 232, 0.4);
}

.auth-error { color: var(--alert-red); font-size: 12px; margin-top: 10px; display: none; }
.auth-toggle { margin-top: 18px; font-size: 13px; color: var(--text-secondary); }
.auth-toggle span { color: #8ab4f8; font-weight: 600; cursor: pointer; text-decoration: underline; margin-left: 4px; }

/* MAIN APP WRAPPER */
.app-container {
    width: 100vw;
    height: 100vh;
    display: none;
    opacity: 0;
    transition: opacity 0.4s ease;
    z-index: 1;
}

/* SIDEBAR WITH DESKTOP COLLAPSE & MOBILE SLIDE */
.sidebar {
    width: 280px;
    background: var(--bg-sidebar);
    border-right: 1px solid var(--border-subtle);
    display: flex;
    flex-direction: column;
    padding: 16px 12px;
    transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
    z-index: 100;
    flex-shrink: 0;
}

/* COLLAPSED STATE ON DESKTOP */
.sidebar.collapsed {
    margin-left: -280px;
}

.sidebar-top { display: flex; align-items: center; justify-content: space-between; margin-bottom: 20px; padding: 0 6px; }
.logo-area { display: flex; align-items: center; gap: 10px; font-weight: 700; font-size: 17px; cursor: pointer; }
.logo-area svg { transition: transform 0.3s ease; }
.logo-area:hover svg { transform: rotate(18deg) scale(1.15); }
.logo-area span { background: linear-gradient(90deg, #4285f4, #9b72cb, #d96570); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }

.new-chat-btn {
    display: flex;
    align-items: center;
    gap: 10px;
    background: #282a2c;
    color: var(--text-primary);
    border: none;
    padding: 12px 16px;
    border-radius: 24px;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    margin-bottom: 18px;
    transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}
.new-chat-btn:hover {
    background: #37393b;
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
}

.sidebar-section-title {
    font-size: 11px;
    font-weight: 700;
    color: var(--text-muted);
    letter-spacing: 0.8px;
    text-transform: uppercase;
    padding: 8px 10px 4px;
}

.sidebar-scroll { flex: 1; overflow-y: auto; padding-right: 4px; }
.sidebar-scroll::-webkit-scrollbar { width: 4px; }
.sidebar-scroll::-webkit-scrollbar-thumb { background: #333; border-radius: 4px; }

.history-item, .task-side-item {
    padding: 9px 12px;
    border-radius: 10px;
    font-size: 13px;
    color: var(--text-secondary);
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 4px;
    cursor: pointer;
    transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
    gap: 8px;
}
.history-item:hover, .task-side-item:hover {
    background: var(--bg-surface-hover);
    color: #fff;
    transform: translateX(3px);
}

.history-item.active {
    background: rgba(66, 133, 244, 0.18);
    color: #8ab4f8;
    font-weight: 500;
    border-left: 3px solid #8ab4f8;
}

.hist-title {
    flex: 1;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    text-align: left;
}

.hist-del-btn {
    background: transparent;
    border: none;
    color: var(--text-muted);
    font-size: 14px;
    padding: 2px 6px;
    border-radius: 4px;
    cursor: pointer;
    opacity: 0.6;
    transition: all 0.2s;
}
.hist-del-btn:hover {
    color: var(--alert-red);
    opacity: 1;
    background: rgba(234, 67, 53, 0.15);
    transform: scale(1.2);
}

.task-side-item small { color: #8ab4f8; font-size: 11px; font-weight: 600; }

.sidebar-bottom {
    padding-top: 12px;
    border-top: 1px solid var(--border-subtle);
    display: flex;
    flex-direction: column;
    gap: 6px;
}

.side-btn {
    display: flex;
    align-items: center;
    gap: 10px;
    background: none;
    border: none;
    color: var(--text-secondary);
    padding: 9px 12px;
    border-radius: 10px;
    font-size: 13px;
    font-weight: 500;
    cursor: pointer;
    text-align: left;
    transition: all 0.2s;
}
.side-btn:hover {
    background: var(--bg-surface-hover);
    color: #fff;
    transform: translateX(3px);
}

/* MAIN CONTENT AREA */
.main-chat-area {
    flex: 1;
    display: flex;
    flex-direction: column;
    height: 100vh;
    position: relative;
    background: var(--bg-main);
    overflow: hidden;
}

/* TOP HEADER */
.main-header {
    height: 60px;
    padding: 0 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid var(--border-subtle);
    backdrop-filter: blur(10px);
}

.header-title-box { display: flex; align-items: center; gap: 10px; }

.mobile-menu-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    background: #1e1f20;
    border: 1px solid var(--border-subtle);
    color: #fff;
    width: 36px;
    height: 36px;
    border-radius: 50%;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.2s;
}
.mobile-menu-btn:hover {
    background: #282a2c;
    border-color: #55575b;
    transform: scale(1.08);
}

.gemini-model-pill {
    display: flex;
    align-items: center;
    gap: 8px;
    background: #1e1f20;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 500;
    color: var(--text-secondary);
    cursor: pointer;
    border: 1px solid var(--border-subtle);
    transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}
.gemini-model-pill:hover {
    border-color: #55575b;
    color: #fff;
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
}

.gemini-status-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: var(--success-green);
    box-shadow: 0 0 8px var(--success-green);
    animation: statusPulse 2s infinite;
}

@keyframes statusPulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.6; transform: scale(0.9); }
}

/* USER PROFILE BADGE (CLICKABLE) */
.user-profile-badge {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 14px;
    font-weight: 500;
    color: var(--text-secondary);
    cursor: pointer;
    padding: 4px 10px 4px 14px;
    border-radius: 24px;
    background: #1e1f20;
    border: 1px solid var(--border-subtle);
    transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}
.user-profile-badge:hover {
    background: #282a2c;
    border-color: #55575b;
    color: #fff;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
}

.user-avatar-circle {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background: linear-gradient(135deg, #4285f4, #9b72cb);
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 14px;
    box-shadow: 0 0 10px rgba(66, 133, 244, 0.4);
}

/* CHAT CANVAS / SCROLL FEED */
.chat-scroll-container {
    flex: 1;
    overflow-y: auto;
    padding: 24px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.chat-scroll-container::-webkit-scrollbar { width: 6px; }
.chat-scroll-container::-webkit-scrollbar-thumb { background: #2d2f31; border-radius: 4px; }

.chat-inner-bounds {
    width: 100%;
    max-width: 820px;
    display: flex;
    flex-direction: column;
    gap: 24px;
}

/* HERO GREETING (GEMINI STYLE) */
.greeting-hero {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 40px 0 20px;
    animation: fadeIn 0.6s ease;
}

.gemini-gradient-text {
    font-size: 48px;
    font-weight: 600;
    letter-spacing: -1px;
    background: linear-gradient(90deg, #4285f4 0%, #9b72cb 45%, #d96570 85%);
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 6px;
    animation: textShimmer 8s ease infinite alternate;
}

@keyframes textShimmer {
    0% { background-position: 0% 50%; }
    100% { background-position: 100% 50%; }
}

.greeting-sub {
    font-size: 26px;
    font-weight: 500;
    color: #444746;
    margin-bottom: 40px;
}

/* QUICK ACTION CHIPS */
.action-chips-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 14px;
    width: 100%;
}

.chip-card {
    background: #1e1f20;
    border: 1px solid #2d2f31;
    border-radius: 16px;
    padding: 18px 16px;
    cursor: pointer;
    transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 110px;
    position: relative;
    overflow: hidden;
}

.chip-card::after {
    content: '';
    position: absolute;
    top: 0; left: -100%; width: 100%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.05), transparent);
    transition: left 0.6s ease;
}

.chip-card:hover {
    background: #282a2c;
    border-color: #55575b;
    transform: translateY(-4px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
}

.chip-card:hover::after {
    left: 100%;
}

.chip-text { font-size: 13px; font-weight: 500; color: var(--text-primary); line-height: 1.4; }
.chip-icon { align-self: flex-end; font-size: 20px; transition: transform 0.3s ease; }
.chip-card:hover .chip-icon { transform: scale(1.2); }

/* MESSAGE BUBBLES WITH SMOOTH ENTRANCE ANIMATION */
.message-row {
    display: flex;
    gap: 16px;
    width: 100%;
    animation: messageSlideIn 0.35s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

@keyframes messageSlideIn {
    from { opacity: 0; transform: translateY(14px); }
    to { opacity: 1; transform: translateY(0); }
}

.user-row { justify-content: flex-end; }

.msg-avatar {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
}

.gemini-avatar {
    background: linear-gradient(135deg, #4285f4, #9b72cb, #d96570);
    box-shadow: 0 0 10px rgba(155, 114, 203, 0.3);
}
.gemini-avatar svg { width: 18px; height: 18px; fill: #fff; }

.gemini-avatar.speaking-pulse {
    animation: avatarPulseGlow 1.2s ease-in-out infinite alternate;
}
@keyframes avatarPulseGlow {
    0% { transform: scale(1); box-shadow: 0 0 10px rgba(66, 133, 244, 0.6); }
    100% { transform: scale(1.15); box-shadow: 0 0 25px rgba(217, 101, 112, 0.9); }
}

.user-bubble {
    background: #282a2c;
    color: #fff;
    padding: 12px 18px;
    border-radius: 20px 20px 4px 20px;
    font-size: 15px;
    line-height: 1.5;
    max-width: 75%;
    font-weight: 500;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

.bot-content {
    flex: 1;
    font-size: 15px;
    line-height: 1.65;
    color: #e3e3e3;
    padding-top: 4px;
}

.bot-content b { color: #fff; }

.app-launched-card {
    background: rgba(66, 133, 244, 0.1);
    border: 1px solid rgba(66, 133, 244, 0.35);
    border-radius: 12px;
    padding: 10px 14px;
    margin-top: 8px;
    display: inline-flex;
    align-items: center;
    gap: 10px;
    font-size: 13px;
    font-weight: 600;
    color: #8ab4f8;
    animation: fadeIn 0.4s ease;
}

/* SOUNDWAVE VISUALIZER BARS */
.soundwave-box {
    display: flex;
    align-items: center;
    gap: 3px;
    height: 16px;
}
.sound-bar {
    width: 3px;
    height: 100%;
    background: linear-gradient(180deg, #4285f4, #9b72cb, #d96570);
    border-radius: 4px;
    animation: soundBarBounce 0.8s ease-in-out infinite alternate;
}
.sound-bar:nth-child(1) { animation-delay: 0.1s; height: 35%; }
.sound-bar:nth-child(2) { animation-delay: 0.3s; height: 85%; }
.sound-bar:nth-child(3) { animation-delay: 0.5s; height: 55%; }
.sound-bar:nth-child(4) { animation-delay: 0.2s; height: 100%; }
.sound-bar:nth-child(5) { animation-delay: 0.4s; height: 45%; }

@keyframes soundBarBounce {
    0% { transform: scaleY(0.25); opacity: 0.6; }
    100% { transform: scaleY(1); opacity: 1; }
}

/* AI SPEAKING BANNER PILL */
.ai-speaking-banner {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: rgba(66, 133, 244, 0.15);
    border: 1px solid rgba(66, 133, 244, 0.4);
    color: #8ab4f8;
    padding: 6px 16px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: 600;
    margin-bottom: 8px;
    cursor: pointer;
    transition: all 0.2s;
    animation: fadeIn 0.3s ease;
}
.ai-speaking-banner:hover {
    background: rgba(234, 67, 53, 0.2);
    border-color: rgba(234, 67, 53, 0.5);
    color: #ff8a80;
}

/* VOICE STATUS PILL */
.voice-status-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(234, 67, 53, 0.15);
    border: 1px solid rgba(234, 67, 53, 0.4);
    color: #ff8a80;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: 600;
    margin-bottom: 8px;
    animation: fadeIn 0.3s ease;
}
.voice-wave-dot {
    width: 8px;
    height: 8px;
    background: #ea4335;
    border-radius: 50%;
    animation: dotPulse 1s infinite alternate;
}
@keyframes dotPulse {
    0% { transform: scale(0.8); opacity: 0.5; }
    100% { transform: scale(1.3); opacity: 1; }
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(6px); }
    to { opacity: 1; transform: translateY(0); }
}

/* THINKING MULTI-COLOR DANCING DOTS */
.thinking-wave-container {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    margin-right: 8px;
}
.think-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    animation: thinkWaveAnim 1.4s infinite ease-in-out both;
}
.think-dot:nth-child(1) { background: #4285f4; animation-delay: -0.32s; }
.think-dot:nth-child(2) { background: #9b72cb; animation-delay: -0.16s; }
.think-dot:nth-child(3) { background: #d96570; animation-delay: 0s; }

@keyframes thinkWaveAnim {
    0%, 80%, 100% { transform: scale(0.6); opacity: 0.4; }
    40% { transform: scale(1.25); opacity: 1; }
}

/* FLOATING INPUT CAPSULE (GEMINI STYLE) */
.input-dock-wrapper {
    width: 100%;
    max-width: 820px;
    margin: 0 auto;
    padding: 12px 20px 20px;
}

.input-capsule {
    background: #1e1f20;
    border: 1px solid #333538;
    border-radius: 30px;
    padding: 8px 14px 8px 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
    transition: all 0.25s cubic-bezier(0.16, 1, 0.3, 1);
}

.input-capsule:focus-within {
    border-color: #55575b;
    background: #232527;
    box-shadow: 0 6px 30px rgba(0, 0, 0, 0.6), 0 0 15px rgba(66, 133, 244, 0.15);
}

.main-input {
    flex: 1;
    background: transparent;
    border: none;
    color: #fff;
    font-size: 15px;
    outline: none;
    font-family: inherit;
}
.main-input::placeholder { color: var(--text-muted); }

.input-btn-group { display: flex; align-items: center; gap: 6px; }

.icon-btn {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    border: none;
    background: transparent;
    color: var(--text-secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    font-size: 16px;
    transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}
.icon-btn:hover {
    background: #333538;
    color: #fff;
    transform: scale(1.08);
}

.send-active-btn {
    background: #8ab4f8 !important;
    color: #0b1528 !important;
}
.send-active-btn:hover {
    box-shadow: 0 0 15px rgba(138, 180, 248, 0.5);
    transform: scale(1.1);
}

.mic-active-glow {
    background: var(--alert-red) !important;
    color: #fff !important;
    animation: micPulse 1s infinite;
}

@keyframes micPulse {
    0% { box-shadow: 0 0 0 0 rgba(234, 67, 53, 0.8); }
    70% { box-shadow: 0 0 0 12px rgba(234, 67, 53, 0); }
    100% { box-shadow: 0 0 0 0 rgba(234, 67, 53, 0); }
}

/* GENERAL MODAL OVERLAY STYLES */
.modal-overlay {
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    background: rgba(0, 0, 0, 0.7);
    backdrop-filter: blur(10px);
    z-index: 10001;
    display: none;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.settings-box {
    background: #1e1f20;
    border: 1px solid #333538;
    border-radius: 28px;
    padding: 30px;
    width: 100%;
    max-width: 520px;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.8);
    animation: modalPopIn 0.35s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

@keyframes modalPopIn {
    from { opacity: 0; transform: scale(0.92) translateY(12px); }
    to { opacity: 1; transform: scale(1) translateY(0); }
}

.modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border-subtle);
}
.modal-title { font-size: 18px; font-weight: 700; color: #fff; }
.modal-close {
    background: none;
    border: none;
    color: var(--text-muted);
    font-size: 22px;
    cursor: pointer;
    transition: all 0.2s;
    width: 32px;
    height: 32px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
}
.modal-close:hover {
    color: #fff;
    background: #282a2c;
    transform: scale(1.15);
}

/* PROFILE & MULTI-ACCOUNT CARD */
.profile-card {
    background: #1e1f20;
    border: 1px solid #333538;
    border-radius: 28px;
    padding: 28px;
    width: 100%;
    max-width: 480px;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.85);
    animation: modalPopIn 0.3s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

.profile-active-box {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 16px;
    background: #131314;
    border-radius: 20px;
    border: 1px solid var(--border-subtle);
    margin-bottom: 16px;
}

.profile-large-avatar {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background: linear-gradient(135deg, #4285f4, #9b72cb, #d96570);
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 26px;
    font-weight: 700;
    box-shadow: 0 0 20px rgba(155, 114, 203, 0.4);
    flex-shrink: 0;
}

.profile-info { flex: 1; overflow: hidden; }
.profile-name-row { display: flex; align-items: center; gap: 8px; }
.profile-name { font-size: 17px; font-weight: 700; color: #fff; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
.profile-edit-btn { background: none; border: none; color: var(--text-muted); cursor: pointer; font-size: 14px; padding: 2px; }
.profile-edit-btn:hover { color: #8ab4f8; }

.profile-email { font-size: 13px; color: var(--text-secondary); margin: 2px 0 6px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
.profile-status-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 11px;
    color: #8ab4f8;
    background: rgba(66, 133, 244, 0.12);
    padding: 3px 10px;
    border-radius: 12px;
    font-weight: 500;
}

.profile-stats-row {
    display: flex;
    gap: 10px;
    margin-bottom: 18px;
}

.stat-item {
    flex: 1;
    background: #18191a;
    border: 1px solid var(--border-subtle);
    border-radius: 14px;
    padding: 10px;
    text-align: center;
}
.stat-val { font-size: 16px; font-weight: 700; color: #fff; }
.stat-lbl { font-size: 11px; color: var(--text-muted); margin-top: 2px; }

.profile-section-title {
    font-size: 11px;
    font-weight: 700;
    color: var(--text-muted);
    letter-spacing: 0.8px;
    text-transform: uppercase;
    margin-bottom: 8px;
    padding-left: 4px;
}

.account-list {
    max-height: 160px;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    gap: 6px;
    margin-bottom: 12px;
}
.account-list::-webkit-scrollbar { width: 4px; }
.account-list::-webkit-scrollbar-thumb { background: #333; border-radius: 4px; }

.account-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 14px;
    background: #18191a;
    border: 1px solid var(--border-subtle);
    border-radius: 14px;
    cursor: pointer;
    transition: all 0.2s;
}
.account-item:hover {
    background: var(--bg-surface-hover);
    border-color: #444746;
}
.account-item.active {
    border-color: #8ab4f8;
    background: rgba(66, 133, 244, 0.1);
}

.account-left { display: flex; align-items: center; gap: 12px; overflow: hidden; }
.account-mini-avatar {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background: linear-gradient(135deg, #4285f4, #9b72cb);
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 13px;
    flex-shrink: 0;
}
.account-details { overflow: hidden; text-align: left; }
.account-det-name { font-size: 13px; font-weight: 600; color: #fff; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
.account-det-email { font-size: 11px; color: var(--text-muted); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }

.add-account-btn {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    background: transparent;
    border: 1px dashed #444746;
    color: #8ab4f8;
    padding: 11px;
    border-radius: 16px;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s;
}
.add-account-btn:hover {
    background: rgba(66, 133, 244, 0.08);
    border-color: #8ab4f8;
}

/* FOCUS TARGET LOCK OVERLAY */
#targetLockModal {
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    background: rgba(14, 16, 20, 0.96);
    backdrop-filter: blur(12px);
    z-index: 99999;
    display: none;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.lock-dialog {
    background: #1e1f20;
    border: 2px solid var(--alert-red);
    border-radius: 28px;
    padding: 40px;
    max-width: 460px;
    width: 100%;
    text-align: center;
    box-shadow: 0 0 60px rgba(234, 67, 53, 0.5);
    animation: lockShake 0.5s ease;
}

@keyframes lockShake {
    0%, 100% { transform: scale(1); }
    25% { transform: scale(1.03); }
    75% { transform: scale(0.97); }
}

.lock-title { font-size: 20px; font-weight: 700; color: #fff; margin-bottom: 10px; }
.lock-desc { font-size: 14px; color: var(--text-secondary); line-height: 1.5; margin-bottom: 24px; }
.lock-btn {
    background: var(--alert-red);
    color: #fff;
    border: none;
    padding: 14px 28px;
    border-radius: 24px;
    font-size: 14px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    width: 100%;
}
.lock-btn:hover { opacity: 0.9; transform: scale(1.02); }

/* RESPONSIVE DESIGN */
@media (max-width: 768px) {
    .sidebar {
        position: fixed;
        left: -280px;
        top: 0;
        bottom: 0;
        height: 100vh;
        box-shadow: 10px 0 30px rgba(0,0,0,0.5);
    }
    .sidebar.open { transform: translateX(280px); }
    .gemini-gradient-text { font-size: 36px; }
    .greeting-sub { font-size: 20px; }
    .action-chips-grid { grid-template-columns: 1fr; }
}
</style>
</head>
<body>

<!-- AUTHENTICATION SCREEN -->
<div id="loginScreen">
    <div class="gemini-auth-card">
        <!-- CANCEL/CUT BUTTON WHEN ADDING ANOTHER ACCOUNT -->
        <button type="button" class="modal-close" id="loginCancelBtn" onclick="cancelAddAccount()" style="display:none; position:absolute; top:18px; right:18px;" title="Cancel & Return">✕</button>

        <div class="gemini-sparkle-logo">
            <svg viewBox="0 0 24 24"><path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z"/></svg>
        </div>
        <div class="auth-title" id="formTitle">Welcome to Shadow AI</div>
        <div class="auth-sub" id="formSub">Sign in to your Shadow AI workspace</div>

        <div class="auth-input-group" id="nameGroup" style="display:none;">
            <label>FULL NAME</label>
            <input type="text" id="regName" class="auth-input" placeholder="e.g. Dhruv Dubey">
        </div>

        <div class="auth-input-group">
            <label>EMAIL ADDRESS</label>
            <input type="email" id="authEmail" class="auth-input" placeholder="user@gmail.com" value="dhruv@shadow.ai">
        </div>

        <div class="auth-input-group">
            <label>PASSWORD</label>
            <input type="password" id="authPass" class="auth-input" placeholder="Enter your password" value="password123">
            <button type="button" class="toggle-pass-btn" onclick="togglePasswordVisibility()">👁️</button>
        </div>

        <div class="auth-error" id="authError">Invalid credentials.</div>

        <button class="auth-btn" id="authBtn" onclick="handleAuth()">Sign in</button>

        <div class="auth-toggle" id="toggleText">
            Don't have an account? <span onclick="switchAuthMode('register')">Create one</span>
        </div>
    </div>
</div>

<!-- MAIN DASHBOARD -->
<div class="app-container" id="appContainer">
    <!-- COLLAPSIBLE SIDEBAR -->
    <aside class="sidebar" id="sidebar">
        <div class="sidebar-top">
            <div class="logo-area" onclick="startNewChat()">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="none"><path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z" fill="url(#sparkleGrad)"/><defs><linearGradient id="sparkleGrad" x1="0" y1="0" x2="24" y2="24" gradientUnits="userSpaceOnUse"><stop stop-color="#4285F4"/><stop offset="0.5" stop-color="#9B72CB"/><stop offset="1" stop-color="#D96570"/></linearGradient></defs></svg>
                <span>Shadow AI</span>
            </div>
            <!-- SIDEBAR CUT / COLLAPSE BUTTON -->
            <button class="icon-btn" onclick="toggleSidebar()" title="Close Sidebar (Cut)">✕</button>
        </div>

        <button class="new-chat-btn" onclick="startNewChat()">
            <span style="font-size:16px;">＋</span> New chat
        </button>

        <div class="sidebar-scroll">
            <div class="sidebar-section-title">SCHEDULED TARGETS</div>
            <div id="sideTaskList">
                <div style="font-size:12px; color:var(--text-muted); padding:6px 12px;">No targets set.</div>
            </div>

            <div class="sidebar-section-title" style="margin-top: 14px;">RECENT CHATS</div>
            <div id="sideRecentList">
                <div style="font-size:12px; color:var(--text-muted); padding:6px 12px;">No past chats yet.</div>
            </div>
        </div>

        <div class="sidebar-bottom">
            <button class="side-btn" onclick="openProfileModal()">
                👤 <span>Profile & Accounts</span>
            </button>
            <button class="side-btn" onclick="openSettingsModal()">
                ⚙️ <span>API & Config</span>
            </button>
            <button class="side-btn" onclick="openSettingsModal('voiceTab')">
                🎙️ <span>AI Voice: <b id="sideVoiceLabel">Female</b></span>
            </button>
            <button class="side-btn" onclick="play432Tone()">
                🕉️ <span>432Hz Sound</span>
            </button>
            <button class="side-btn" onclick="clearChatHistory()" style="color:var(--alert-red);">
                🗑️ <span>Clear All History</span>
            </button>
            <button class="side-btn" onclick="logoutUser()">
                🚪 <span>Log out</span>
            </button>
        </div>
    </aside>

    <!-- MAIN CHAT CANVAS -->
    <main class="main-chat-area">
        <!-- TOP HEADER -->
        <header class="main-header">
            <div class="header-title-box">
                <!-- HAMBURGER BUTTON TO REOPEN SIDEBAR WHEN COLLAPSED -->
                <button class="mobile-menu-btn" id="headerMenuBtn" onclick="toggleSidebar()" title="Toggle Sidebar">☰</button>
                <div class="gemini-model-pill" onclick="openSettingsModal()" title="AI Engine Settings">
                    <span class="gemini-status-dot" id="headerStatusDot"></span>
                    <span id="headerModelName">Shadow AI (Free Engine)</span>
                    <span style="font-size:10px; color:var(--text-muted);">▾</span>
                </div>
                <div class="gemini-model-pill" onclick="openSettingsModal('voiceTab')" title="Change Voice Persona">
                    <span id="headerVoiceIcon">👩</span>
                    <span id="headerVoiceName">Female Voice</span>
                    <span style="font-size:10px; color:var(--text-muted);">▾</span>
                </div>
            </div>

            <!-- CLICKABLE USER PROFILE BADGE -->
            <div class="user-profile-badge" onclick="openProfileModal()" title="View Profile & Switch Accounts">
                <span id="userNameBadge">Dhruv</span>
                <div class="user-avatar-circle" id="userAvatarText">D</div>
            </div>
        </header>

        <!-- CHAT FEED -->
        <div class="chat-scroll-container" id="chatScroll">
            <div class="chat-inner-bounds" id="chatFeed">
                <!-- HERO GREETING (Shown when conversation is empty) -->
                <div class="greeting-hero" id="greetingHero">
                    <div class="gemini-gradient-text" id="greetingName">Hello, Dhruv</div>
                    <div class="greeting-sub">I am Shadow AI. How can I help you today?</div>

                    <!-- QUICK ACTION PROMPTS -->
                    <div class="action-chips-grid">
                        <div class="chip-card" onclick="submitQuickPrompt('Open YouTube')">
                            <div class="chip-text">Launch YouTube application</div>
                            <div class="chip-icon">▶️</div>
                        </div>
                        <div class="chip-card" onclick="submitQuickPrompt('Open WhatsApp')">
                            <div class="chip-text">Open WhatsApp Web</div>
                            <div class="chip-icon">💬</div>
                        </div>
                        <div class="chip-card" onclick="submitQuickPrompt('Schedule YouTube at 17:00')">
                            <div class="chip-text">Schedule YouTube target at 17:00</div>
                            <div class="chip-icon">⏰</div>
                        </div>
                        <div class="chip-card" onclick="submitQuickPrompt('What is the speed of light?')">
                            <div class="chip-text">Explain scientific facts and math</div>
                            <div class="chip-icon">✨</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- FLOATING INPUT CAPSULE -->
        <div class="input-dock-wrapper">
            <!-- SPEAKING / VOICE STATUS INDICATORS -->
            <div style="display:flex; justify-content:center; gap:8px;">
                <div id="voiceStatusPill" class="voice-status-pill" style="display:none;">
                    <span class="voice-wave-dot"></span>
                    <span id="voiceStatusText">Listening... Speak now</span>
                </div>
                <div id="aiSpeakingBanner" class="ai-speaking-banner" style="display:none;" onclick="stopSpeaking()" title="Click to Stop Voice">
                    <div class="soundwave-box">
                        <span class="sound-bar"></span>
                        <span class="sound-bar"></span>
                        <span class="sound-bar"></span>
                        <span class="sound-bar"></span>
                        <span class="sound-bar"></span>
                    </div>
                    <span>Shadow AI is speaking (Click to mute)</span>
                </div>
            </div>

            <div class="input-capsule">
                <input type="text" class="main-input" id="userInput" placeholder="Ask Shadow AI, open any app, or schedule a task (e.g. '18:00 par youtube schedule kardo')..." autocomplete="off">
                <div class="input-btn-group">
                    <button class="icon-btn" id="micBtn" onclick="toggleContinuousListening()" title="Voice Input (Speech Recognition)">🎤</button>
                    <button class="icon-btn send-active-btn" id="sendBtn" onclick="processQuery()" title="Send">➤</button>
                </div>
            </div>
            <div style="text-align: center; font-size: 11px; color: var(--text-muted); margin-top: 8px;">
                Shadow AI may display inaccurate info. Powered by Multi-Voice Engine & Neural Assistant.
            </div>
        </div>
    </main>
</div>

<!-- PROFILE & MULTI-ACCOUNT SWITCHER MODAL -->
<div id="profileModal" class="modal-overlay" onclick="onProfileOverlayClick(event)">
    <div class="profile-card">
        <div class="modal-header" style="margin-bottom:16px;">
            <div class="modal-title">👤 Account & Profile</div>
            <button class="modal-close" onclick="closeProfileModal()" title="Close Profile (Cut)">✕</button>
        </div>

        <!-- CURRENT ACTIVE ACCOUNT BANNER -->
        <div class="profile-active-box">
            <div class="profile-large-avatar" id="profAvatar">D</div>
            <div class="profile-info">
                <div class="profile-name-row">
                    <span class="profile-name" id="profName">Dhruv Dubey</span>
                    <button class="profile-edit-btn" onclick="promptEditName()" title="Edit Name">✏️</button>
                </div>
                <div class="profile-email" id="profEmail">dhruv@shadow.ai</div>
                <div class="profile-status-badge">
                    <span class="gemini-status-dot"></span> Active Session • Shadow AI
                </div>
            </div>
        </div>

        <!-- STATS BAR -->
        <div class="profile-stats-row">
            <div class="stat-item">
                <div class="stat-val" id="profChatCount">0</div>
                <div class="stat-lbl">Conversations</div>
            </div>
            <div class="stat-item">
                <div class="stat-val" id="profTargetCount">0</div>
                <div class="stat-lbl">Targets</div>
            </div>
            <div class="stat-item">
                <div class="stat-val" id="profEngineLbl">FREE</div>
                <div class="stat-lbl">AI Engine</div>
            </div>
        </div>

        <!-- MULTI-ACCOUNT LIST -->
        <div class="profile-section-title">SWITCH ACCOUNTS ON THIS DEVICE</div>
        <div class="account-list" id="accountListContainer">
            <!-- Dynamically rendered -->
        </div>

        <!-- ADD ANOTHER ACCOUNT -->
        <button class="add-account-btn" onclick="openAddAccountScreen()">
            <span style="font-size:18px;">＋</span> Add another account
        </button>

        <!-- LOGOUT BUTTONS -->
        <div style="border-top: 1px solid var(--border-subtle); margin-top: 16px; padding-top: 16px; display:flex; gap:10px;">
            <button class="auth-btn" style="flex:1; background:#282a2c; color:#fff;" onclick="logoutUser()">
                🚪 Sign out
            </button>
            <button class="auth-btn" style="flex:1; background:#ea4335; color:#fff;" onclick="logoutAllAccounts()">
                🚪 Sign out all
            </button>
        </div>
    </div>
</div>

<!-- SETTINGS, AI ENGINE & VOICE PERSONA MODAL -->
<div id="settingsModal" class="modal-overlay" onclick="onSettingsOverlayClick(event)">
    <div class="settings-box">
        <div class="modal-header">
            <div class="modal-title">⚙️ AI Engine & Voice Persona</div>
            <button class="modal-close" onclick="closeSettingsModal()" title="Close Settings (Cut)">✕</button>
        </div>

        <!-- VOICE PERSONA SETTING -->
        <div style="margin-bottom: 20px; background: #18191a; padding: 16px; border-radius: 16px; border: 1px solid var(--border-subtle);">
            <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:8px;">
                <label style="font-size:12px; color:var(--text-secondary); font-weight:700; letter-spacing:0.5px;">AI VOICE PERSONA</label>
                <button type="button" class="auth-btn" style="width:auto; padding:6px 14px; margin:0; font-size:12px; background:#2d2f31; color:#fff;" onclick="testVoiceProfile()">🔊 Test Voice</button>
            </div>
            <select id="modalVoiceProfile" class="auth-input" onchange="onVoiceProfileChange()">
                <option value="female">👩 Shadow Female (Natural & Calm)</option>
                <option value="male">👨 Shadow Male (Deep & Powerful)</option>
                <option value="indian">🇮🇳 Indian Accent (Hinglish / Natural)</option>
                <option value="cyber">🤖 Cyber Synth (Robotic AI Jarvis)</option>
                <option value="cosmic">🌌 Cosmic Whisper (Relaxed & Soft)</option>
            </select>
            <div style="font-size:11px; color:var(--text-muted); margin-top:6px;">
                Choose the voice persona Shadow AI uses when reading responses aloud.
            </div>
        </div>

        <!-- AI ENGINE PROVIDER -->
        <div style="margin-bottom: 16px;">
            <label style="font-size:12px; color:var(--text-secondary); display:block; margin-bottom:6px; font-weight:600;">ACTIVE AI PROVIDER</label>
            <select id="modalApiProvider" class="auth-input" onchange="onModalProviderChange()">
                <option value="free">⚡ Free Built-in AI (No API Key Required - Instant)</option>
                <option value="gemini">Google Gemini API (gemini-2.5-flash / gemini-2.0)</option>
                <option value="groq">Groq Cloud API (Llama-3.3-70b)</option>
                <option value="openai">OpenAI API (gpt-4o-mini)</option>
            </select>
        </div>

        <div id="modalKeyContainer" style="display:none; margin-bottom: 16px;">
            <label style="font-size:12px; color:var(--text-secondary); display:block; margin-bottom:6px; font-weight:600;">API KEY</label>
            <input type="password" id="modalApiKeyInput" class="auth-input" placeholder="Paste your API key here...">
        </div>

        <div style="display:flex; gap:10px; margin-top: 24px;">
            <button class="auth-btn" style="flex:1;" onclick="saveModalSettings()">Save Settings</button>
            <button class="auth-btn" style="background:#282a2c; color:#fff; width:auto; padding:0 20px;" onclick="testCurrentApi()">🧪 Test API</button>
        </div>
    </div>
</div>

<!-- FOCUS TARGET LOCK MODAL -->
<div id="targetLockModal">
    <div class="lock-dialog">
        <div style="font-size:42px; margin-bottom:12px;">⏰</div>
        <div class="lock-title">SCHEDULED TARGET ACTIVE</div>
        <div class="lock-desc" id="lockMessage">Time to focus on your objective!</div>
        <button class="lock-btn" onclick="fulfillTarget()">EXECUTE & UNLOCK</button>
    </div>
</div>

<script>
// STATE
let currentUser = localStorage.getItem("geminiActiveUser") || "Dhruv Dubey";
let currentActiveEmail = localStorage.getItem("geminiActiveEmail") || "dhruv@shadow.ai";
let currentSessionId = null;
let scheduledTargets = JSON.parse(localStorage.getItem("geminiFocusTargets")) || [];
let activeLockTarget = null;
let reminderInterval = null;
let recognition = null;
let isListening = false;
let isSpeaking = false;
let apiProvider = localStorage.getItem("jarvisApiProvider") || "free";
let apiKey = localStorage.getItem("jarvisApiKey") || "";
let selectedVoiceProfile = localStorage.getItem("shadowVoiceProfile") || "female";
const audioCtx = new (window.AudioContext || window.webkitAudioContext)();
let availableVoices = [];

// VOICE PERSONA DEFINITIONS
const VOICE_PROFILES = {
    "female": {
        name: "Female Voice",
        label: "Female",
        icon: "👩",
        pitch: 1.05,
        rate: 1.0
    },
    "male": {
        name: "Male Voice",
        label: "Male",
        icon: "👨",
        pitch: 0.78,
        rate: 0.92
    },
    "indian": {
        name: "Indian Voice",
        label: "Indian",
        icon: "🇮🇳",
        pitch: 1.0,
        rate: 0.98
    },
    "cyber": {
        name: "Cyber Synth",
        label: "Cyber",
        icon: "🤖",
        pitch: 1.4,
        rate: 1.15
    },
    "cosmic": {
        name: "Cosmic Whisper",
        label: "Cosmic",
        icon: "🌌",
        pitch: 0.85,
        rate: 0.82
    }
};

// APP DIRECTORY FOR SMART OPEN COMMANDS
const APP_DIRECTORY = {
    "youtube": "https://www.youtube.com",
    "yt": "https://www.youtube.com",
    "google": "https://www.google.com",
    "whatsapp": "https://web.whatsapp.com",
    "instagram": "https://www.instagram.com",
    "insta": "https://www.instagram.com",
    "github": "https://www.github.com",
    "gmail": "https://mail.google.com",
    "mail": "https://mail.google.com",
    "chatgpt": "https://chatgpt.com",
    "spotify": "https://open.spotify.com",
    "netflix": "https://www.netflix.com",
    "twitter": "https://twitter.com",
    "x": "https://x.com",
    "linkedin": "https://www.linkedin.com",
    "maps": "https://maps.google.com",
    "reddit": "https://www.reddit.com",
    "amazon": "https://www.amazon.in",
    "flipkart": "https://www.flipkart.com",
    "canva": "https://www.canva.com",
    "telegram": "https://web.telegram.org",
    "facebook": "https://www.facebook.com",
    "fb": "https://www.facebook.com"
};

// MULTI-ACCOUNT MANAGEMENT
function getAccountList() {
    let list = JSON.parse(localStorage.getItem("geminiAccountList")) || [];
    if (!list.length) {
        list = [{ email: "dhruv@shadow.ai", name: "Dhruv Dubey" }];
        localStorage.setItem("geminiAccountList", JSON.stringify(list));
    }
    return list;
}

function saveAccountList(list) {
    localStorage.setItem("geminiAccountList", JSON.stringify(list));
}

// POPULATE BROWSER VOICES ASYNCHRONOUSLY
function populateVoices() {
    if ('speechSynthesis' in window) {
        availableVoices = speechSynthesis.getVoices();
    }
}
populateVoices();
if ('speechSynthesis' in window) {
    speechSynthesis.onvoiceschanged = populateVoices;
}

// INITIALIZATION
window.addEventListener('DOMContentLoaded', () => {
    const activeUser = localStorage.getItem('geminiActiveUser');
    const activeEmail = localStorage.getItem('geminiActiveEmail');
    if (activeUser) {
        authenticateSuccess(activeUser, activeEmail || "dhruv@shadow.ai");
    } else {
        // Show login screen
        document.getElementById("loginScreen").style.display = "flex";
        document.getElementById("loginScreen").style.opacity = "1";
    }
    updateModelHeaderBadge();
    updateVoiceHeaderBadge();
    renderSidebarTargets();
    initSpeechRecognition();
});

// AUTHENTICATION
let authMode = 'login';
let usersDatabase = JSON.parse(localStorage.getItem('geminiUsers')) || {
    "dhruv@shadow.ai": { name: "Dhruv Dubey", password: "password123" }
};

function togglePasswordVisibility() {
    const p = document.getElementById("authPass");
    p.type = p.type === 'password' ? 'text' : 'password';
}

function switchAuthMode(mode) {
    authMode = mode;
    document.getElementById("authError").style.display = "none";
    if (mode === 'register') {
        document.getElementById("formTitle").innerText = "Create your Account";
        document.getElementById("formSub").innerText = "Get started with Shadow AI";
        document.getElementById("nameGroup").style.display = "block";
        document.getElementById("authBtn").innerText = "Create Account";
        document.getElementById("toggleText").innerHTML = 'Already have an account? <span onclick="switchAuthMode(\'login\')">Sign in</span>';
    } else {
        document.getElementById("formTitle").innerText = "Welcome to Shadow AI";
        document.getElementById("formSub").innerText = "Sign in to your Shadow AI workspace";
        document.getElementById("nameGroup").style.display = "none";
        document.getElementById("authBtn").innerText = "Sign in";
        document.getElementById("toggleText").innerHTML = 'Don\'t have an account? <span onclick="switchAuthMode(\'register\')">Create one</span>';
    }
}

function handleAuth() {
    const email = document.getElementById("authEmail").value.trim().toLowerCase();
    const pass = document.getElementById("authPass").value.trim();

    if (!email || !pass) { showAuthError("Please fill in all fields."); return; }

    if (authMode === 'register') {
        const name = document.getElementById("regName").value.trim();
        if (!name) { showAuthError("Please enter your name."); return; }
        if (usersDatabase[email]) { showAuthError("Account already exists with this email."); return; }

        usersDatabase[email] = { name, password: pass };
        localStorage.setItem("geminiUsers", JSON.stringify(usersDatabase));

        // Add to accounts list
        let accounts = getAccountList();
        if (!accounts.some(a => a.email === email)) {
            accounts.push({ email, name });
            saveAccountList(accounts);
        }

        authenticateSuccess(name, email);
    } else {
        if (!usersDatabase[email] || usersDatabase[email].password !== pass) {
            showAuthError("Invalid email or password.");
            return;
        }

        const name = usersDatabase[email].name;
        let accounts = getAccountList();
        if (!accounts.some(a => a.email === email)) {
            accounts.push({ email, name });
            saveAccountList(accounts);
        }

        authenticateSuccess(name, email);
    }
}

function showAuthError(msg) {
    const el = document.getElementById("authError");
    el.innerText = msg;
    el.style.display = "block";
}

function authenticateSuccess(name, email) {
    currentUser = name || "Dhruv";
    currentActiveEmail = email || currentActiveEmail || "dhruv@shadow.ai";
    localStorage.setItem("geminiActiveUser", currentUser);
    localStorage.setItem("geminiActiveEmail", currentActiveEmail);

    document.getElementById("userNameBadge").innerText = currentUser;
    document.getElementById("userAvatarText").innerText = currentUser.charAt(0).toUpperCase();
    document.getElementById("greetingName").innerText = `Hello, ${currentUser}`;

    const loginScreen = document.getElementById("loginScreen");
    loginScreen.style.opacity = "0";
    setTimeout(() => {
        loginScreen.style.display = "none";
        document.getElementById("loginCancelBtn").style.display = "none";

        const app = document.getElementById("appContainer");
        app.style.display = "flex";
        setTimeout(() => app.style.opacity = "1", 50);

        migrateOldHistory();
        renderSidebarRecentChats();

        const sessions = getSessions();
        if (sessions.length > 0) {
            loadSession(sessions[0].id);
        } else {
            startNewChat();
        }
    }, 350);
}

// INSTANT LOGOUT (NO BROKEN RELOAD)
function logoutUser() {
    localStorage.removeItem("geminiActiveUser");
    localStorage.removeItem("geminiActiveEmail");
    currentUser = "";
    currentActiveEmail = "";

    if ('speechSynthesis' in window) speechSynthesis.cancel();
    if (toneOsc) { toneOsc.stop(); toneOsc = null; }

    closeProfileModal();
    closeSettingsModal();
    document.getElementById("sidebar").classList.remove("open");
    document.getElementById("sidebar").classList.remove("collapsed");

    const app = document.getElementById("appContainer");
    const loginScreen = document.getElementById("loginScreen");
    document.getElementById("loginCancelBtn").style.display = "none";

    app.style.opacity = "0";
    setTimeout(() => {
        app.style.display = "none";
        loginScreen.style.display = "flex";
        setTimeout(() => loginScreen.style.opacity = "1", 50);
    }, 300);
}

function logoutAllAccounts() {
    if (confirm("Are you sure you want to sign out of all accounts on this device?")) {
        localStorage.removeItem("geminiActiveUser");
        localStorage.removeItem("geminiActiveEmail");
        localStorage.removeItem("geminiAccountList");
        logoutUser();
    }
}

// PROFILE & MULTI-ACCOUNT MODAL CONTROLLERS
function openProfileModal() {
    renderProfileModal();
    document.getElementById("profileModal").style.display = "flex";
}

function closeProfileModal() {
    document.getElementById("profileModal").style.display = "none";
}

function onProfileOverlayClick(e) {
    if (e.target.id === "profileModal") closeProfileModal();
}

function onSettingsOverlayClick(e) {
    if (e.target.id === "settingsModal") closeSettingsModal();
}

function renderProfileModal() {
    document.getElementById("profAvatar").innerText = currentUser ? currentUser.charAt(0).toUpperCase() : "U";
    document.getElementById("profName").innerText = currentUser || "User";
    document.getElementById("profEmail").innerText = currentActiveEmail || "user@shadow.ai";
    document.getElementById("profChatCount").innerText = getSessions().length;
    document.getElementById("profTargetCount").innerText = scheduledTargets.length;
    document.getElementById("profEngineLbl").innerText = apiProvider.toUpperCase();

    const container = document.getElementById("accountListContainer");
    container.innerHTML = "";
    const accounts = getAccountList();

    accounts.forEach(acc => {
        const isActive = acc.email === currentActiveEmail;
        const item = document.createElement("div");
        item.className = `account-item ${isActive ? 'active' : ''}`;
        item.onclick = () => switchAccount(acc.email);
        item.innerHTML = `
            <div class="account-left">
                <div class="account-mini-avatar">${acc.name.charAt(0).toUpperCase()}</div>
                <div class="account-details">
                    <div class="account-det-name">${escapeHtml(acc.name)} ${isActive ? '<span style="color:#8ab4f8; font-size:11px; margin-left:4px;">(Active)</span>' : ''}</div>
                    <div class="account-det-email">${escapeHtml(acc.email)}</div>
                </div>
            </div>
            ${!isActive ? `<button class="hist-del-btn" onclick="removeAccountFromDevice(event, '${acc.email}')" title="Remove account">✕</button>` : '<span style="color:#34a853; font-size:14px; font-weight:700;">✓</span>'}
        `;
        container.appendChild(item);
    });
}

function switchAccount(email) {
    if (email === currentActiveEmail) {
        closeProfileModal();
        return;
    }
    const accounts = getAccountList();
    const target = accounts.find(a => a.email === email);
    if (!target) return;

    currentUser = target.name;
    currentActiveEmail = target.email;
    localStorage.setItem("geminiActiveUser", currentUser);
    localStorage.setItem("geminiActiveEmail", currentActiveEmail);

    document.getElementById("userNameBadge").innerText = currentUser;
    document.getElementById("userAvatarText").innerText = currentUser.charAt(0).toUpperCase();
    document.getElementById("greetingName").innerText = `Hello, ${currentUser}`;

    closeProfileModal();
    renderSidebarRecentChats();
    startNewChat();
    appendBotMessage(`Switched to account <b>${currentUser}</b> (${currentActiveEmail}). Welcome back!`);
    speak(`Switched account to ${currentUser}.`);
}

function removeAccountFromDevice(e, email) {
    e.stopPropagation();
    let accounts = getAccountList();
    if (accounts.length <= 1) {
        alert("You cannot remove the only saved account. Use 'Sign out' instead.");
        return;
    }
    if (confirm(`Remove ${email} from this device?`)) {
        accounts = accounts.filter(a => a.email !== email);
        saveAccountList(accounts);
        if (email === currentActiveEmail) {
            switchAccount(accounts[0].email);
        } else {
            renderProfileModal();
        }
    }
}

function openAddAccountScreen() {
    closeProfileModal();
    document.getElementById("loginCancelBtn").style.display = "flex";
    document.getElementById("authEmail").value = "";
    document.getElementById("authPass").value = "";
    document.getElementById("authError").style.display = "none";
    switchAuthMode("login");

    const app = document.getElementById("appContainer");
    const loginScreen = document.getElementById("loginScreen");
    app.style.opacity = "0";
    setTimeout(() => {
        app.style.display = "none";
        loginScreen.style.display = "flex";
        setTimeout(() => loginScreen.style.opacity = "1", 50);
    }, 300);
}

function cancelAddAccount() {
    const loginScreen = document.getElementById("loginScreen");
    loginScreen.style.opacity = "0";
    setTimeout(() => {
        loginScreen.style.display = "none";
        document.getElementById("loginCancelBtn").style.display = "none";
        const app = document.getElementById("appContainer");
        app.style.display = "flex";
        setTimeout(() => app.style.opacity = "1", 50);
    }, 300);
}

function promptEditName() {
    const newName = prompt("Enter your new display name:", currentUser);
    if (newName && newName.trim() && newName.trim() !== currentUser) {
        const cleanName = newName.trim();
        currentUser = cleanName;
        localStorage.setItem("geminiActiveUser", currentUser);

        if (usersDatabase[currentActiveEmail]) {
            usersDatabase[currentActiveEmail].name = currentUser;
            localStorage.setItem("geminiUsers", JSON.stringify(usersDatabase));
        }

        let accounts = getAccountList();
        const acc = accounts.find(a => a.email === currentActiveEmail);
        if (acc) {
            acc.name = currentUser;
            saveAccountList(accounts);
        }

        document.getElementById("userNameBadge").innerText = currentUser;
        document.getElementById("userAvatarText").innerText = currentUser.charAt(0).toUpperCase();
        document.getElementById("greetingName").innerText = `Hello, ${currentUser}`;
        renderProfileModal();
        appendBotMessage(`Profile updated! Your display name is now <b>${currentUser}</b>.`);
        speak(`Profile updated. Hello, ${currentUser}.`);
    }
}

// TOGGLE SIDEBAR (CUT / EXPAND ON DESKTOP & MOBILE)
function toggleSidebar() {
    const sb = document.getElementById("sidebar");
    if (window.innerWidth < 768) {
        sb.classList.toggle("open");
    } else {
        sb.classList.toggle("collapsed");
    }
}

// SETTINGS & VOICE MODAL
function openSettingsModal(focusTab) {
    document.getElementById("modalApiProvider").value = apiProvider;
    document.getElementById("modalApiKeyInput").value = apiKey;
    document.getElementById("modalVoiceProfile").value = selectedVoiceProfile;
    onModalProviderChange();
    document.getElementById("settingsModal").style.display = "flex";
}

function closeSettingsModal() {
    document.getElementById("settingsModal").style.display = "none";
}

function onModalProviderChange() {
    const prov = document.getElementById("modalApiProvider").value;
    const keyBox = document.getElementById("modalKeyContainer");
    if (prov === "free") {
        keyBox.style.display = "none";
    } else {
        keyBox.style.display = "block";
    }
}

function onVoiceProfileChange() {
    selectedVoiceProfile = document.getElementById("modalVoiceProfile").value;
    localStorage.setItem("shadowVoiceProfile", selectedVoiceProfile);
    updateVoiceHeaderBadge();
}

function saveModalSettings() {
    apiProvider = document.getElementById("modalApiProvider").value;
    apiKey = document.getElementById("modalApiKeyInput").value.trim();
    selectedVoiceProfile = document.getElementById("modalVoiceProfile").value;
    localStorage.setItem("jarvisApiProvider", apiProvider);
    localStorage.setItem("jarvisApiKey", apiKey);
    localStorage.setItem("shadowVoiceProfile", selectedVoiceProfile);
    updateModelHeaderBadge();
    updateVoiceHeaderBadge();
    closeSettingsModal();
    appendBotMessage(`Settings saved! Active Engine: <b>${apiProvider.toUpperCase()}</b> | Voice Persona: <b>${VOICE_PROFILES[selectedVoiceProfile].name}</b>.`);
    speak(`Settings saved, ${currentUser}. Active engine is ${apiProvider}.`);
}

function updateModelHeaderBadge() {
    const nameEl = document.getElementById("headerModelName");
    const dot = document.getElementById("headerStatusDot");
    if (apiProvider === "free") {
        nameEl.innerText = "Shadow AI (Free Engine)";
        dot.style.background = "var(--success-green)";
    } else {
        nameEl.innerText = `Shadow AI (${apiProvider.toUpperCase()})`;
        dot.style.background = apiKey ? "var(--success-green)" : "var(--alert-red)";
    }
}

function updateVoiceHeaderBadge() {
    const prof = VOICE_PROFILES[selectedVoiceProfile] || VOICE_PROFILES["female"];
    const iconEl = document.getElementById("headerVoiceIcon");
    const nameEl = document.getElementById("headerVoiceName");
    const sideLabel = document.getElementById("sideVoiceLabel");
    if (iconEl) iconEl.innerText = prof.icon;
    if (nameEl) nameEl.innerText = prof.name;
    if (sideLabel) sideLabel.innerText = prof.label;
}

// MULTI-SESSION CHAT HISTORY SYSTEM
function getSessions() {
    return JSON.parse(localStorage.getItem(`shadowSessions_${currentUser}`)) || [];
}

function saveSessions(sessions) {
    localStorage.setItem(`shadowSessions_${currentUser}`, JSON.stringify(sessions));
}

function migrateOldHistory() {
    const old = JSON.parse(localStorage.getItem(`geminiChat_${currentUser}`)) || [];
    const sessions = getSessions();
    if (old.length > 0 && sessions.length === 0) {
        const firstUser = old.find(m => m.type === 'user-bubble')?.text || "Previous Chat";
        const title = firstUser.replace(/<[^>]*>?/gm, '').trim().substring(0, 24) || "Previous Chat";
        const migrated = {
            id: "session_" + Date.now(),
            title: title,
            timestamp: Date.now(),
            messages: old
        };
        saveSessions([migrated]);
    }
}

function renderSidebarRecentChats() {
    const list = document.getElementById("sideRecentList");
    list.innerHTML = "";
    const sessions = getSessions();
    if (!sessions.length) {
        list.innerHTML = `<div style="font-size:12px; color:var(--text-muted); padding:8px 12px;">No past chats yet.</div>`;
        return;
    }
    sessions.forEach(sess => {
        const div = document.createElement("div");
        div.className = `history-item ${sess.id === currentSessionId ? 'active' : ''}`;
        div.onclick = () => loadSession(sess.id);

        const safeTitle = escapeHtml(sess.title);
        div.innerHTML = `
            <span class="hist-title" title="${safeTitle}">💬 ${safeTitle}</span>
            <button class="hist-del-btn" onclick="deleteSession(event, '${sess.id}')" title="Delete chat (Cut)">✕</button>
        `;
        list.appendChild(div);
    });
}

function loadSession(sessionId) {
    const sessions = getSessions();
    const target = sessions.find(s => s.id === sessionId);
    if (!target) return;
    currentSessionId = target.id;
    renderSidebarRecentChats();

    const hero = document.getElementById("greetingHero");
    if (hero) hero.style.display = "none";

    const feed = document.getElementById("chatFeed");
    feed.innerHTML = "";

    target.messages.forEach(item => {
        if (item.type === 'user-bubble') {
            const row = document.createElement("div");
            row.className = "message-row user-row";
            row.innerHTML = `<div class="user-bubble">${item.text}</div>`;
            feed.appendChild(row);
        } else {
            const row = document.createElement("div");
            row.className = "message-row";
            row.innerHTML = `
                <div class="msg-avatar gemini-avatar">
                    <svg viewBox="0 0 24 24"><path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z"/></svg>
                </div>
                <div class="bot-content">${item.text}</div>
            `;
            feed.appendChild(row);
        }
    });
    scrollToBottom();
    if (window.innerWidth < 768) {
        document.getElementById("sidebar").classList.remove("open");
    }
}

function startNewChat() {
    currentSessionId = null;
    renderSidebarRecentChats();

    const feed = document.getElementById("chatFeed");
    feed.innerHTML = `
        <div class="greeting-hero" id="greetingHero">
            <div class="gemini-gradient-text" id="greetingName">Hello, ${currentUser}</div>
            <div class="greeting-sub">I am Shadow AI. How can I help you today?</div>

            <div class="action-chips-grid">
                <div class="chip-card" onclick="submitQuickPrompt('Open YouTube')">
                    <div class="chip-text">Launch YouTube application</div>
                    <div class="chip-icon">▶️</div>
                </div>
                <div class="chip-card" onclick="submitQuickPrompt('Open WhatsApp')">
                    <div class="chip-text">Open WhatsApp Web</div>
                    <div class="chip-icon">💬</div>
                </div>
                <div class="chip-card" onclick="submitQuickPrompt('Schedule YouTube at 17:00')">
                    <div class="chip-text">Schedule YouTube target at 17:00</div>
                    <div class="chip-icon">⏰</div>
                </div>
                <div class="chip-card" onclick="submitQuickPrompt('What is the speed of light?')">
                    <div class="chip-text">Explain scientific facts and math</div>
                    <div class="chip-icon">✨</div>
                </div>
            </div>
        </div>
    `;
    const inp = document.getElementById("userInput");
    inp.value = "";
    inp.focus();
    if (window.innerWidth < 768) {
        document.getElementById("sidebar").classList.remove("open");
    }
}

function deleteSession(e, sessionId) {
    e.stopPropagation();
    let sessions = getSessions();
    sessions = sessions.filter(s => s.id !== sessionId);
    saveSessions(sessions);
    if (currentSessionId === sessionId) {
        startNewChat();
    } else {
        renderSidebarRecentChats();
    }
}

function clearChatHistory() {
    if (confirm("Are you sure you want to clear all chat history?")) {
        localStorage.removeItem(`shadowSessions_${currentUser}`);
        localStorage.removeItem(`geminiChat_${currentUser}`);
        startNewChat();
    }
}

function persistMessage(text, type) {
    let sessions = getSessions();
    let activeSess = sessions.find(s => s.id === currentSessionId);

    if (!activeSess) {
        currentSessionId = "session_" + Date.now();
        const clean = text.replace(/<[^>]*>?/gm, '').trim();
        const title = clean.length > 25 ? clean.substring(0, 25) + "..." : clean || "New Conversation";
        activeSess = {
            id: currentSessionId,
            title: title,
            timestamp: Date.now(),
            messages: []
        };
        sessions.unshift(activeSess);
    }

    activeSess.messages.push({ text, type });
    saveSessions(sessions);
    renderSidebarRecentChats();
}

// SMART APP OPENER & INTENT DETECTOR
function detectAppOpenIntent(query) {
    const q = query.toLowerCase().trim();
    
    const hasOpenWord = /(open|launch|start|kholo|chalao|play|chala do|khol do)/i.test(q);
    if (!hasOpenWord) return null;

    for (const [key, url] of Object.entries(APP_DIRECTORY)) {
        const regex = new RegExp(`(^|\\s)${key}(\\s|$)`, 'i');
        if (regex.test(q)) {
            return { name: key.toUpperCase(), url: url };
        }
    }

    const words = q.split(/\s+/);
    for (const w of words) {
        if (w.includes(".") && !w.startsWith("http") && w.length > 3) {
            return { name: w, url: `https://${w}` };
        }
    }

    return null;
}

// SMART NATURAL LANGUAGE SCHEDULE PARSER
function parseNaturalSchedule(query) {
    const q = query.toLowerCase();

    const isSchedule = q.includes("schedule") || q.includes("remind") || q.includes("target") ||
                       q.includes("baje") || q.includes("alarm");

    if (!isSchedule) return null;

    let timeMatch = q.match(/([0-9]{1,2}):([0-9]{2})/);
    let targetTime = null;

    if (timeMatch) {
        targetTime = `${String(timeMatch[1]).padStart(2, '0')}:${String(timeMatch[2]).padStart(2, '0')}`;
    } else {
        let singleHour = q.match(/([0-9]{1,2})\s*(am|pm|baje)/i);
        if (singleHour) {
            let h = parseInt(singleHour[1]);
            if (singleHour[2].toLowerCase() === 'pm' && h < 12) h += 12;
            targetTime = `${String(h).padStart(2, '0')}:00`;
        }
    }

    if (!targetTime) return null;

    let appName = "google";
    for (const key in APP_DIRECTORY) {
        if (q.includes(key)) {
            appName = key;
            break;
        }
    }

    return {
        task: query.replace(/(schedule|kardo|remind me to|set alarm for)/gi, '').trim() || `Focus Target: ${appName}`,
        time: targetTime,
        app: appName,
        completed: false
    };
}

// QUERY PROCESSING
async function processQuery() {
    const inputEl = document.getElementById("userInput");
    const query = inputEl.value.trim();
    if (!query) return;

    const hero = document.getElementById("greetingHero");
    if (hero) hero.style.display = "none";

    appendUserMessage(query);
    inputEl.value = "";

    // 1. Instant App Open Intent
    const appIntent = detectAppOpenIntent(query);
    if (appIntent) {
        const reply = `Opening <b>${appIntent.name}</b> for you now, ${currentUser}!`;
        appendBotMessage(reply + `<br><div class="app-launched-card">🚀 Launched ${appIntent.name} (${appIntent.url})</div>`);
        speak(`Opening ${appIntent.name} for you, ${currentUser}.`);
        window.open(appIntent.url, "_blank");
        return;
    }

    // 2. Schedule Target Intent
    const scheduleIntent = parseNaturalSchedule(query);
    if (scheduleIntent) {
        scheduledTargets.push(scheduleIntent);
        localStorage.setItem("geminiFocusTargets", JSON.stringify(scheduledTargets));
        renderSidebarTargets();
        const reply = `Target locked for <b>${scheduleIntent.time}</b> on <b>${scheduleIntent.app.toUpperCase()}</b>! I will lock the screen and notify you when it's time.`;
        appendBotMessage(reply);
        speak(`Target scheduled for ${scheduleIntent.time} on ${scheduleIntent.app}.`);
        return;
    }

    // 3. AI / Math / Knowledge Engine
    appendBotThinking();

    try {
        const aiResponse = await fetchAIResponse(query);
        removeBotThinking();
        appendBotMessage(aiResponse);
        speak(aiResponse);
    } catch (err) {
        removeBotThinking();
        const fallback = fetchLocalFallback(query);
        appendBotMessage(`<b>[Note: ${err.message}]</b><br>${fallback}`);
        speak(fallback);
    }
}

function submitQuickPrompt(text) {
    document.getElementById("userInput").value = text;
    processQuery();
}

// AI ENGINE (FREE BUILT-IN + GEMINI / GROQ / OPENAI)
async function fetchAIResponse(query) {
    const systemPrompt = `You are Shadow AI, a super-intelligent, polite, and helpful personal AI assistant. The user's name is ${currentUser}. Address the user warmly. Keep your voice responses concise (1 to 3 sentences unless detailed code or tutorials are asked). Answer in the same language as the user (English, Hindi, or Hinglish). Do not use excessive asterisks or markdown symbols so it sounds natural when read aloud.`;

    const sessions = getSessions();
    const activeSess = sessions.find(s => s.id === currentSessionId);
    let recentTurns = [];
    if (activeSess && activeSess.messages) {
        recentTurns = activeSess.messages.slice(-6).map(item => ({
            role: item.type === 'user-bubble' ? 'user' : 'assistant',
            content: item.text.replace(/<[^>]*>?/gm, '').trim()
        }));
    }

    // Free Mode (Pollinations OpenAI engine - zero key needed)
    if (apiProvider === "free" || !apiKey) {
        const response = await fetch("https://text.pollinations.ai/", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({
                messages: [
                    { role: "system", content: systemPrompt },
                    ...recentTurns,
                    { role: "user", content: query }
                ],
                model: "openai"
            })
        });

        if (!response.ok) {
            const getRes = await fetch(`https://text.pollinations.ai/${encodeURIComponent(query)}?system=${encodeURIComponent(systemPrompt)}&model=openai`);
            if (!getRes.ok) throw new Error("Free AI network issue.");
            return (await getRes.text()).trim();
        }
        return (await response.text()).trim();
    }

    // Google Gemini API
    if (apiProvider === "gemini") {
        const models = ["gemini-2.5-flash", "gemini-2.0-flash", "gemini-1.5-flash"];
        for (const model of models) {
            const url = `https://generativelanguage.googleapis.com/v1beta/models/${model}:generateContent?key=${encodeURIComponent(apiKey)}`;
            const res = await fetch(url, {
                method: "POST",
                headers: { "Content-Type": "application/json" },
                body: JSON.stringify({
                    systemInstruction: { parts: [{ text: systemPrompt }] },
                    contents: [{ role: "user", parts: [{ text: query }] }]
                })
            });
            const data = await res.json();
            if (res.ok && data.candidates?.[0]?.content?.parts?.[0]?.text) {
                return data.candidates[0].content.parts[0].text.trim();
            }
        }
        throw new Error("Gemini API call failed. Check key in settings.");
    }

    // Groq or OpenAI
    const endpoint = apiProvider === "groq"
        ? "https://api.groq.com/openai/v1/chat/completions"
        : "https://api.openai.com/v1/chat/completions";
    const model = apiProvider === "groq" ? "llama-3.3-70b-versatile" : "gpt-4o-mini";

    const res = await fetch(endpoint, {
        method: "POST",
        headers: {
            "Content-Type": "application/json",
            "Authorization": `Bearer ${apiKey}`
        },
        body: JSON.stringify({
            model: model,
            messages: [{ role: "system", content: systemPrompt }, { role: "user", content: query }]
        })
    });
    const data = await res.json();
    if (!res.ok) throw new Error(data.error?.message || "API request failed");
    return data.choices[0].message.content.trim();
}

function fetchLocalFallback(query) {
    try {
        let clean = query.toLowerCase().replace(/[^0-9+\-*/().]/g, '');
        if (clean && /[0-9]/.test(clean)) {
            let res = Function(`'use strict'; return (${clean})`)();
            if (typeof res === 'number') return `${currentUser}, the answer is ${res}.`;
        }
    } catch(e){}
    return `${currentUser}, I am Shadow AI. Ask me to open any app (e.g. 'open youtube') or schedule targets!`;
}

// DOM HELPERS
function appendUserMessage(text) {
    const feed = document.getElementById("chatFeed");
    const row = document.createElement("div");
    row.className = "message-row user-row";
    row.innerHTML = `<div class="user-bubble">${text}</div>`;
    feed.appendChild(row);
    scrollToBottom();
    persistMessage(text, "user-bubble");
}

function appendBotMessage(html) {
    const feed = document.getElementById("chatFeed");
    const row = document.createElement("div");
    row.className = "message-row";
    row.innerHTML = `
        <div class="msg-avatar gemini-avatar" id="currentBotAvatar">
            <svg viewBox="0 0 24 24"><path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z"/></svg>
        </div>
        <div class="bot-content">${html}</div>
    `;
    feed.appendChild(row);
    scrollToBottom();
    persistMessage(html, "bot-bubble");
}

function appendBotThinking() {
    const feed = document.getElementById("chatFeed");
    const row = document.createElement("div");
    row.className = "message-row thinking-row";
    row.id = "thinkingRow";
    row.innerHTML = `
        <div class="msg-avatar gemini-avatar">
            <svg viewBox="0 0 24 24"><path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z"/></svg>
        </div>
        <div class="bot-content" style="display:flex; align-items:center;">
            <div class="thinking-wave-container">
                <span class="think-dot"></span>
                <span class="think-dot"></span>
                <span class="think-dot"></span>
            </div>
            <span style="color:var(--text-muted); font-style:italic;">Shadow AI is thinking...</span>
        </div>
    `;
    feed.appendChild(row);
    scrollToBottom();
}

function removeBotThinking() {
    const el = document.getElementById("thinkingRow");
    if (el) el.remove();
}

function scrollToBottom() {
    const container = document.getElementById("chatScroll");
    container.scrollTop = container.scrollHeight;
}

// TARGETS IN SIDEBAR
function renderSidebarTargets() {
    const list = document.getElementById("sideTaskList");
    list.innerHTML = "";
    if (!scheduledTargets.length) {
        list.innerHTML = "<div style='font-size:12px; color:var(--text-muted); padding:6px 12px;'>No targets set.</div>";
        return;
    }
    scheduledTargets.forEach((t, i) => {
        const div = document.createElement("div");
        div.className = "task-side-item";
        div.innerHTML = `
            <div>
                <div>${escapeHtml(t.task)}</div>
                <small>${t.time} • ${t.app.toUpperCase()}</small>
            </div>
            <button class="hist-del-btn" onclick="deleteTarget(${i})" title="Delete target (Cut)">✕</button>
        `;
        list.appendChild(div);
    });
}

function deleteTarget(i) {
    scheduledTargets.splice(i, 1);
    localStorage.setItem("geminiFocusTargets", JSON.stringify(scheduledTargets));
    renderSidebarTargets();
}

// SCHEDULE CHECKER
setInterval(() => {
    const now = new Date();
    const currentHM = `${String(now.getHours()).padStart(2, '0')}:${String(now.getMinutes()).padStart(2, '0')}`;

    scheduledTargets.forEach(target => {
        if (!target.completed && target.time === currentHM && !activeLockTarget) {
            triggerTargetLock(target);
        }
    });
}, 1000);

function triggerTargetLock(target) {
    activeLockTarget = target;
    document.getElementById("lockMessage").innerHTML = `<b>${currentUser}</b>, your target time <b>(${target.time})</b> is active!<br>Objective: "${escapeHtml(target.task)}"<br>Application: <b>${target.app.toUpperCase()}</b>`;
    document.getElementById("targetLockModal").style.display = "flex";
    playAlarmTone();
    speak(`Attention ${currentUser}! Your scheduled target is active. Please execute ${target.app} now.`);

    reminderInterval = setInterval(() => {
        playAlarmTone();
        speak(`${currentUser}, please execute ${target.app} to fulfill your target.`);
    }, 10000);
}

function fulfillTarget() {
    if (!activeLockTarget) return;
    const url = APP_DIRECTORY[activeLockTarget.app] || `https://www.google.com/search?q=${encodeURIComponent(activeLockTarget.app)}`;
    window.open(url, "_blank");

    activeLockTarget.completed = true;
    localStorage.setItem("geminiFocusTargets", JSON.stringify(scheduledTargets));
    renderSidebarTargets();

    clearInterval(reminderInterval);
    document.getElementById("targetLockModal").style.display = "none";
    speak(`Target executed successfully, ${currentUser}.`);
    activeLockTarget = null;
}

// ADVANCED VOICE SYNTHESIS WITH MULTIPLE PERSONAS
function getVoiceForProfile(profileKey) {
    if (!availableVoices.length) populateVoices();
    
    if (profileKey === "female") {
        return availableVoices.find(v => 
            v.lang.startsWith("en") && (
                v.name.includes("Female") || v.name.includes("Samantha") || 
                v.name.includes("Zira") || v.name.includes("Google US English") || 
                v.name.includes("Victoria") || v.name.includes("Karen")
            )
        ) || availableVoices.find(v => v.lang.startsWith("en")) || availableVoices[0];
    }
    
    if (profileKey === "male") {
        return availableVoices.find(v => 
            v.lang.startsWith("en") && (
                v.name.includes("Male") || v.name.includes("David") || 
                v.name.includes("George") || v.name.includes("Google UK English Male") || 
                v.name.includes("Guy") || v.name.includes("James") || v.name.includes("Mark")
            )
        ) || availableVoices.find(v => v.lang.startsWith("en")) || availableVoices[0];
    }
    
    if (profileKey === "indian") {
        return availableVoices.find(v => 
            v.lang === "en-IN" || v.lang === "hi-IN" || 
            v.name.includes("India") || v.name.includes("Heera") || 
            v.name.includes("Neerja") || v.name.includes("Veena")
        ) || availableVoices.find(v => v.lang.startsWith("en")) || availableVoices[0];
    }
    
    if (profileKey === "cyber") {
        return availableVoices.find(v => v.lang.startsWith("en") && (v.name.includes("Google") || v.name.includes("Daniel") || v.name.includes("David"))) || availableVoices[0];
    }
    
    if (profileKey === "cosmic") {
        return availableVoices.find(v => v.lang.startsWith("en") && (v.name.includes("Natural") || v.name.includes("Google") || v.name.includes("Samantha"))) || availableVoices[0];
    }

    return availableVoices[0];
}

function speak(text) {
    if (!('speechSynthesis' in window)) return;
    speechSynthesis.cancel();

    const clean = text.replace(/<[^>]*>?/gm, '');
    const ut = new SpeechSynthesisUtterance(clean);
    
    const v = getVoiceForProfile(selectedVoiceProfile);
    if (v) ut.voice = v;

    const prof = VOICE_PROFILES[selectedVoiceProfile] || VOICE_PROFILES["female"];
    ut.pitch = prof.pitch;
    ut.rate = prof.rate;

    ut.onstart = () => {
        isSpeaking = true;
        updateSpeakingUI(true);
    };

    ut.onend = () => {
        isSpeaking = false;
        updateSpeakingUI(false);
    };

    ut.onerror = () => {
        isSpeaking = false;
        updateSpeakingUI(false);
    };

    speechSynthesis.speak(ut);
}

function stopSpeaking() {
    if ('speechSynthesis' in window) {
        speechSynthesis.cancel();
    }
    isSpeaking = false;
    updateSpeakingUI(false);
}

function updateSpeakingUI(speaking) {
    const banner = document.getElementById("aiSpeakingBanner");
    if (banner) banner.style.display = speaking ? "inline-flex" : "none";

    const avatars = document.querySelectorAll(".gemini-avatar");
    if (avatars.length) {
        const lastAvatar = avatars[avatars.length - 1];
        if (speaking) {
            lastAvatar.classList.add("speaking-pulse");
        } else {
            avatars.forEach(a => a.classList.remove("speaking-pulse"));
        }
    }
}

function testVoiceProfile() {
    const prof = VOICE_PROFILES[selectedVoiceProfile] || VOICE_PROFILES["female"];
    speak(`Hello ${currentUser}! I am Shadow AI. This is my ${prof.name}. How do I sound to you?`);
}

// SPEECH RECOGNITION (VOICE INPUT)
function initSpeechRecognition() {
    const SpeechRec = window.SpeechRecognition || window.webkitSpeechRecognition;
    if (!SpeechRec) {
        console.warn("SpeechRecognition unsupported in this browser.");
        return;
    }
    try {
        recognition = new SpeechRec();
        recognition.lang = navigator.language || "en-IN";
        recognition.continuous = false;
        recognition.interimResults = true;
        recognition.maxAlternatives = 1;

        recognition.onstart = () => {
            isListening = true;
            document.getElementById("micBtn").classList.add("mic-active-glow");
            const voicePill = document.getElementById("voiceStatusPill");
            if (voicePill) voicePill.style.display = "inline-flex";
            const voiceText = document.getElementById("voiceStatusText");
            if (voiceText) voiceText.innerText = "Listening... Speak your command now!";
            document.getElementById("userInput").placeholder = "🎙️ Listening... Speak now (e.g. 'Open YouTube' or 'Schedule 18:00')";
        };

        recognition.onresult = (e) => {
            let interimTranscript = '';
            let finalTranscript = '';

            for (let i = e.resultIndex; i < e.results.length; ++i) {
                if (e.results[i].isFinal) {
                    finalTranscript += e.results[i][0].transcript;
                } else {
                    interimTranscript += e.results[i][0].transcript;
                }
            }

            const activeText = finalTranscript || interimTranscript;
            if (activeText) {
                document.getElementById("userInput").value = activeText;
                const voiceText = document.getElementById("voiceStatusText");
                if (voiceText) voiceText.innerText = `Heard: "${activeText}"`;
            }

            if (finalTranscript.trim()) {
                setTimeout(() => {
                    resetVoiceUI();
                    processQuery();
                }, 250);
            }
        };

        recognition.onerror = (e) => {
            console.warn("Speech recognition error:", e.error);
            resetVoiceUI();
            if (e.error === "not-allowed") {
                alert("Microphone permission denied! Please click the lock or camera/mic icon in your browser address bar to allow microphone access.");
            } else if (e.error === "network") {
                alert("Speech recognition network error. Please verify your internet connection.");
            }
        };

        recognition.onend = () => {
            resetVoiceUI();
        };
    } catch(err) {
        console.error("Speech recognition error:", err);
    }
}

function resetVoiceUI() {
    isListening = false;
    const mic = document.getElementById("micBtn");
    if (mic) mic.classList.remove("mic-active-glow");
    const voicePill = document.getElementById("voiceStatusPill");
    if (voicePill) voicePill.style.display = "none";
    const inp = document.getElementById("userInput");
    if (inp) inp.placeholder = "Ask Shadow AI, open any app, or schedule a task (e.g. '18:00 par youtube schedule kardo')...";
}

function toggleContinuousListening() {
    const SpeechRec = window.SpeechRecognition || window.webkitSpeechRecognition;
    if (!SpeechRec) {
        alert("Speech Recognition is not supported by your browser. Please use Chrome, Edge, or Safari.");
        return;
    }
    if (!recognition) initSpeechRecognition();

    if (!isListening) {
        stopSpeaking();
        try {
            recognition.start();
        } catch(e) {
            try {
                recognition.stop();
                setTimeout(() => recognition.start(), 150);
            } catch(err){}
        }
    } else {
        try {
            recognition.stop();
        } catch(e){}
        resetVoiceUI();
    }
}

function playAlarmTone() {
    try {
        if (audioCtx.state === 'suspended') audioCtx.resume();
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = 'sine';
        osc.frequency.setValueAtTime(520, audioCtx.currentTime);
        osc.frequency.exponentialRampToValueAtTime(1040, audioCtx.currentTime + 0.3);
        gain.gain.setValueAtTime(0.1, audioCtx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.3);
        osc.connect(gain); gain.connect(audioCtx.destination);
        osc.start(); osc.stop(audioCtx.currentTime + 0.3);
    } catch(e){}
}

let toneOsc = null;
function play432Tone() {
    if (audioCtx.state === 'suspended') audioCtx.resume();
    if (toneOsc) { toneOsc.stop(); toneOsc = null; appendBotMessage("432Hz Sound Stopped."); return; }
    toneOsc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();
    toneOsc.frequency.setValueAtTime(432, audioCtx.currentTime);
    gain.gain.setValueAtTime(0.05, audioCtx.currentTime);
    toneOsc.connect(gain); gain.connect(audioCtx.destination);
    toneOsc.start();
    appendBotMessage("🕉️ <b>432Hz Harmonic Frequency Playing</b> (Click button again in sidebar to stop).");
}

async function testCurrentApi() {
    try {
        const test = await fetchAIResponse("Respond with only: ONLINE");
        alert(`✅ Test Success: ${test}`);
    } catch(e) {
        alert(`❌ Test Failed: ${e.message}`);
    }
}

function escapeHtml(str) {
    if (!str) return "";
    return String(str).replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;").replace(/"/g, "&quot;");
}

document.getElementById("userInput").addEventListener("keydown", (e) => { if (e.key === "Enter") processQuery(); });
document.getElementById("authPass").addEventListener("keydown", (e) => { if (e.key === "Enter") handleAuth(); });
</script>
</body>
</html>
