<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Educatia de succes</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <link rel="icon" type="image/png" href="https://img.icons8.com/ios-filled/50/000000/open-book.png">
    <style>
        :root {
            --sidebar-width: 220px;
            --sidebar-collapsed: 60px;
            --sidebar-bg: linear-gradient(135deg, #2d3a4b 80%, #4e5d6c 100%);
            --sidebar-bg-dark: linear-gradient(135deg, #1a2028 80%, #2d3a4b 100%);
            --main-bg: #f4f6fb;
            --main-bg-dark: #23272f;
            --main-color: #222;
            --main-color-dark: #e0e4ea;
            --accent: #1abc9c;
        }

        html { scroll-behavior: smooth; }

        body {
            margin: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
            background: var(--main-bg);
            color: var(--main-color);
            min-height: 100vh;
        }    
        .sidebar {
    position: fixed;
    left: 0; top: 0; bottom: 0;
    width: var(--sidebar-width);
    background: var(--sidebar-bg);
    box-shadow: 2px 0 10px rgba(0,0,0,0.07);
    display: flex;
    flex-direction: column;
    padding-top: 40px;
    z-index: 100;
    transition: width 0.3s cubic-bezier(.4,2,.6,1), padding-top 0.3s cubic-bezier(.4,2,.6,1), gap 0.3s cubic-bezier(.4,2,.6,1);
}

       .sidebar.collapsed {
    width: var(--sidebar-collapsed);
    padding-top: 20px;
    gap: 0.2rem;
    transition: width 0.3s cubic-bezier(.4,2,.6,1), padding-top 0.3s cubic-bezier(.4,2,.6,1), gap 0.3s cubic-bezier(.4,2,.6,1);
}

        .sidebar .collapse-btn {
            background: none;
            border: none;
            color: #fff;
            font-size: 1.3rem;
            margin: 0 0 20px 0;
            cursor: pointer;
            align-self: flex-end;
            transition: color 0.2s;
        }

        .sidebar .collapse-btn:hover { color: var(--accent); }

        .sidebar .menu-btn {
            background: none;
            border: none;
            color: #fff;
            font-size: 1.1rem;
            padding: 18px 30px;
            text-align: left;
            cursor: pointer;
            transition: background 0.2s, color 0.2s;
            border-radius: 0 30px 30px 0;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 12px;
            position: relative;
        }

        .sidebar .menu-btn span {
    transition: opacity 0.25s cubic-bezier(.4,2,.6,1), width 0.25s cubic-bezier(.4,2,.6,1), margin 0.25s cubic-bezier(.4,2,.6,1);
    display: inline-block;
    width: auto;
    opacity: 1;
    margin-left: 0.5em;
}

        .sidebar .menu-btn[aria-current="page"] {
            background: #fff;
            color: #2d3a4b;
        }

        .sidebar .menu-btn:hover {
            background: #fff;
            color: #2d3a4b;
        }

        .sidebar.collapsed .menu-btn span {
    opacity: 0;
    width: 0;
    margin-left: 0;
    pointer-events: none;
}
        .sidebar.collapsed .menu-btn {
            justify-content: center;
            padding: 12px 10px;
        }

        .main-content {
            margin-left: var(--sidebar-width);
            padding: 40px 5vw 40px 5vw;
            min-height: 100vh;
            transition: margin-left 0.3s;
        }

        .lobby-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            letter-spacing: 2px;
            animation: fadeInDown 1.2s cubic-bezier(.23,1.01,.32,1) both;
        }

        @keyframes fadeInDown {
            0% { opacity: 0; transform: translateY(-40px);}
            100% { opacity: 1; transform: translateY(0);}
        }
        
        .carousel {
            max-width: 700px;
            margin: 30px auto 30px auto;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 2px 12px rgba(44,62,80,0.09);
            background: #fff;
            position: relative;
            scrollbar-width: none;
        }
        .carousel::-webkit-scrollbar {
            display: none;
}

        .carousel-inner {
            display: flex;
            transition: transform 0.5s cubic-bezier(.23,1.01,.32,1);
        }

        .carousel-slide {
            min-width: 100%;
            box-sizing: border-box;
            padding: 30px 40px;
            text-align: center;
            font-size: 1.2rem;
        }

        .carousel-controls {
            position: absolute;
            top: 50%;
            left: 0; right: 0;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
            pointer-events: none;
        }

        .carousel-btn {
            background: #2d3a4b;
            color: #fff;
            border: none;
            border-radius: 50%;
            width: 36px; height: 36px;
            font-size: 1.3rem;
            cursor: pointer;
            pointer-events: all;
            opacity: 0.8;
            transition: background 0.2s, opacity 0.2s;
        }

        .carousel-btn:hover { background: var(--accent); opacity: 1; }

:root {
    --sidebar-width: 220px;
    --sidebar-collapsed: 60px;
    --sidebar-bg: linear-gradient(135deg, #2d3a4b 80%, #4e5d6c 100%);
    --sidebar-bg-dark: linear-gradient(135deg, #1a2028 80%, #2d3a4b 100%);
    --main-bg: #f4f6fb;
    --main-bg-dark: #23272f;
    --main-color: #222;
    --main-color-dark: #e0e4ea;
    --accent: #1abc9c; /* green for light */
    --accent-dark: #a259e6; /* purple for dark */
    --sidebar-purple: linear-gradient(135deg, #3a1c71 80%, #a259e6 100%);
    --sidebar-purple-dark: linear-gradient(135deg, #1a1028 80%, #3a1c71 100%);
    --section-border: 2px solid #1abc9c;
    --section-border-dark: 2px solid #a259e6;
    --section-bg-dark: #2d2340;
}

body, .sidebar, .main-content, .comments-section, .share-section, .tab-content, .stat-box, .carousel, .intro {
    transition: background 0.5s cubic-bezier(.4,2,.6,1), color 0.5s cubic-bezier(.4,2,.6,1), border-color 0.5s cubic-bezier(.4,2,.6,1);
}

.comments-section, .share-section, .tab-content, .stat-box, .carousel, .intro {
    border: var(--section-border);
    box-sizing: border-box;
}
body.dark-mode .comments-section,
body.dark-mode .share-section,
body.dark-mode .tab-content,
body.dark-mode .stat-box,
body.dark-mode .carousel,
body.dark-mode .intro {
    border: var(--section-border-dark);
}

.see-more-btn,
.reply-btn,
.show-all-replies-btn,
.back-to-comments-btn,
.comment-form button,
.copy-link-btn,
.qr-btn,
.tab-btn.active {
    background: var(--accent);
    transition: background 0.5s cubic-bezier(.4,2,.6,1), color 0.5s cubic-bezier(.4,2,.6,1);
}
body.dark-mode .see-more-btn,
body.dark-mode .reply-btn,
body.dark-mode .show-all-replies-btn,
body.dark-mode .back-to-comments-btn,
body.dark-mode .comment-form button,
body.dark-mode .copy-link-btn,
body.dark-mode .qr-btn,
body.dark-mode .tab-btn.active {
    background: var(--accent-dark);
    color: #fff;
}

body.dark-mode .sidebar {
    background: var(--sidebar-purple-dark);
}
body.dark-mode .sidebar .menu-btn[aria-current="page"],
body.dark-mode .sidebar .menu-btn:hover {
    background: var(--accent-dark);
    color: #fff;
    border-left: 4px solid var(--accent-dark);
}
body.dark-mode .sidebar .menu-btn.active {
    background: var(--accent-dark);
    color: #fff;
    border-left: 4px solid #fff;
}

body.dark-mode .main-content,
body.dark-mode .intro,
body.dark-mode .comments-section,
body.dark-mode .share-section,
body.dark-mode .tab-content,
body.dark-mode .stat-box,
body.dark-mode .carousel {
    background: var(--section-bg-dark) !important;
    color: var(--main-color-dark) !important;
}


        .stats-row {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 30px 0 30px 0;
        }

        .stat-box {
            background: #fff;
            border-radius: 12px;
            box-shadow: 0 1px 8px rgba(44,62,80,0.06);
            padding: 1.2rem 2.2rem;
            text-align: center;
            font-size: 1.1rem;
            min-width: 120px;
        }

        .stat-box .stat-num {
            font-size: 2rem;
            font-weight: bold;
            color: var(--accent);
        }

        .authors-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .author {
            font-size: 1.1rem;
            color: #4e5d6c;
            font-weight: 500;
        }

        .intro {
            background: #fff;
            border-radius: 18px;
            box-shadow: 0 2px 12px rgba(44,62,80,0.07);
            padding: 2rem;
            margin-bottom: 2.5rem;
            font-size: 1.35rem;
            line-height: 1.7;
        }

        .section-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: #2d3a4b;
        }

        .comments-section, .share-section {
            background: #fff;
            border-radius: 14px;
            box-shadow: 0 1px 8px rgba(44,62,80,0.06);
            padding: 1.5rem;
            margin-bottom: 2rem;
        }

        .comments-list {
            margin: 0 0 1rem 0;
            padding: 0;
            list-style: none;
        }

        .comments-list li {
            border-bottom: 1px solid #e0e4ea;
            padding: 0.5rem 0;
            display: flex;
            align-items: flex-start;
            gap: 10px;
            justify-content: space-between;
        }

        .comment-content { flex: 1; }

       .comment-form {
          display: flex;
         gap: 10px;
         align-items: stretch;
}

        .comment-form input, .comment-form textarea {
            flex: 1;
            padding: 8px 12px;
            border-radius: 6px;
            border: 1px solid #cfd8dc;
            font-size: 1rem;
        }

.comment-form input[type="text"] {
    flex: 0 0 90px;
    max-width: 90px;
    min-width: 60px;
    height: 40px;
    box-sizing: border-box;
}
    
.comment-form textarea {
    flex: 1 1 100%;
    min-width: 0;
    width: 100%;
    max-width: 100%;
    min-height: 40px;
    max-height: 40px;
    height: 40px;
    resize: none;
    overflow-y: auto;
    transition: height 0.2s;
    box-sizing: border-box;
    line-height: 1.4;
    padding-top: 8px;
    padding-bottom: 8px;
}

        .comment-form button {
            height: 40px;
              box-sizing: border-box;
              display: flex;
              align-items: center;
              justify-content: center;
              white-space: nowrap;
              padding: 0 18px;
              font-size: 1rem;
              border-radius: 6px;
              background: #2d3a4b;
              color: #fff;
              border: none;
              cursor: pointer;
              transition: background 0.2s;
}

        .comment-form button:hover { background: #4e5d6c; }

        .share-icons {
            display: flex;
            gap: 18px;
            margin-top: 10px;
        }

        .share-icons i {
            font-size: 1.7rem;
            color: #2d3a4b;
            cursor: pointer;
            transition: color 0.2s, transform 0.2s;
        }

        .share-icons i:hover { color: var(--accent); transform: scale(1.15); }

        .copy-link-btn {
            background: #e0e4ea;
            border: none;
            color: #2d3a4b;
            border-radius: 6px;
            padding: 7px 16px;
            font-size: 1rem;
            cursor: pointer;
            margin-bottom: 10px;
            transition: background 0.2s;
        }

        .copy-link-btn:hover { background: #cfd8dc; }

        .qr-btn {
            background: #e0e4ea;
            border: none;
            color: #2d3a4b;
            border-radius: 6px;
            padding: 7px 16px;
            font-size: 1rem;
            cursor: pointer;
            margin-bottom: 10px;
            margin-left: 8px;
            transition: background 0.2s;
        }

        .qr-btn:hover { background: #cfd8dc; }

        .qr-modal-content { text-align: center; }

        .tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 1.2rem;
        }

        .tab-btn {
            background: #e0e4ea;
            border: none;
            border-radius: 6px 6px 0 0;
            padding: 8px 18px;
            font-size: 1rem;
            cursor: pointer;
            color: #2d3a4b;
            transition: background 0.2s;
        }

        .tab-btn.active {
            background: #fff;
            color: var(--accent);
            font-weight: bold;
        }

        .tab-content {
            background: #fff;
            border-radius: 0 0 12px 12px;
            box-shadow: 0 1px 8px rgba(44,62,80,0.06);
            padding: 1.5rem;
            margin-bottom: 2rem;
        }

        .special-title {
            font-size: 3rem;
            font-weight: 900;
            letter-spacing: 3px;
            color: #1abc9c;
            text-shadow: 2px 2px 0 #2d3a4b, 0 2px 8px #0002;
            margin-bottom: 0.2em;
            font-family: 'Georgia', serif;
            text-align: center;
            line-height: 1.1;
        }

        .special-authors {
            display: flex;
            justify-content: center;
            gap: 40px;
            font-size: 1.2rem;
            font-family: 'Georgia', serif;
            color: #1abc9c;
            font-weight: 700;
            margin-bottom: 1.5rem;
            text-shadow: 1px 1px 0 #2d3a4b;
        }

        .special-authors .subtitle {
            font-size: 1rem;
            color: #4e5d6c;
            font-weight: 400;
            margin-top: 0.2em;
            text-align: center;
            width: 100%;
        }

        .lobby-intro-columns {
            column-count: 3;
            column-gap: 2.5rem;
            text-align: justify;
            font-size: 1.18rem;
            line-height: 1.8;
            background: #fff;
            border-radius: 18px;
            box-shadow: 0 2px 12px rgba(44,62,80,0.07);
            padding: 2rem;
            margin-bottom: 2.5rem;
            margin-top: 1.5rem;
        }
        
        

        .scroll-top-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--accent);
            color: #fff;
            border: none;
            border-radius: 50%;
            width: 48px;
            height: 48px;
            font-size: 2rem;
            cursor: pointer;
            box-shadow: 0 2px 8px #0002;
            display: none;
            z-index: 999;
            transition: background 0.2s;
        }
        .scroll-top-btn:hover {
            background: #159c82;
        }

.comment-form .forbidden-highlight {
    text-decoration: underline wavy #ff0033;
    text-underline-offset: 3px;
    background: none !important;
    color: inherit !important;
    font-weight: inherit;
}
.thumb-btn {
    background: none;
    border: 2px solid #cfd8dc;
    font-size: 1.2em;
    cursor: pointer;
    transition: color 0.2s, border-color 0.2s, background 0.2s;
    margin-right: 8px;
    border-radius: 50%;
    width: 36px;
    height: 36px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    outline: none;
}
.thumb-btn.thumb-up.selected,
.thumb-btn.thumb-up:active {
    color: #fff;
    background: #1abc9c;
    border-color: #1abc9c;
    transition: background 0.2s, color 0.2s, border-color 0.2s;
}
.thumb-btn.thumb-down.selected,
.thumb-btn.thumb-down:active {
    color: #fff;
    background: #ff0033;
    border-color: #ff0033;
    transition: background 0.2s, color 0.2s, border-color 0.2s;
}
.thumb-btn i {
    pointer-events: none;
}
.thumb-btn.selected i {
    font-weight: bold;
}
.reactions {
    gap: 6px;
}


.see-more-btn {
    background: #2d3a4b;
    color: #fff;
    border: none;
    border-radius: 6px;
    padding: 0 18px;
    height: 40px;
    font-size: 1rem;
    cursor: pointer;
    margin-top: 10px;
    transition: background 0.2s, box-shadow 0.2s;
    box-shadow: 0 1px 6px rgba(44,62,80,0.08);
    display: inline-flex;
    align-items: center;
    gap: 8px;
}
.see-more-btn:hover {
    background: #159c82;
    color: #fff;
    box-shadow: 0 2px 12px rgba(44,62,80,0.13);
}

.reply-box button,
.reply-box .show-all-replies-btn,
.reply-btn {
    height: 36px;
    box-sizing: border-box;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    white-space: nowrap;
    padding: 0 16px;
    font-size: 1rem;
    border-radius: 6px;
    background: #2d3a4b;
    color: #fff;
    border: none;
    cursor: pointer;
    transition: background 0.2s;
    margin-left: 8px;
}
.reply-box button:hover,
.reply-box .show-all-replies-btn:hover,
.reply-btn:hover {
    background: #1abc9c;
    color: #fff;
}
.comment-content.reply-open {
    opacity: 0.7;
    font-size: 0.97em;
    transition: opacity 0.2s, font-size 0.2s;
}

.show-all-replies-btn,
.back-to-comments-btn {
    background: #2d3a4b;
    color: #fff;
    border: none;
    border-radius: 6px;
    padding: 0 16px;
    height: 36px;
    font-size: 1rem;
    cursor: pointer;
    transition: background 0.2s, color 0.2s;
    margin-left: 8px;
    margin-bottom: 6px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
}
.show-all-replies-btn:hover,
.back-to-comments-btn:hover {
    background: #1abc9c;
    color: #fff;
}

/* ...existing code... */
@media (max-width: 575.98px) {
    .sidebar {
        width: 100vw !important;
        min-width: 0 !important;
        max-width: 100vw !important;
        height: auto;
        position: fixed;
        left: 0; top: 0; bottom: auto;
        flex-direction: row;
        overflow-x: auto;
        overflow-y: visible;
        padding-top: 0;
        gap: 0;
        z-index: 1000;
    }
    .sidebar.collapsed {
        width: 100vw !important;
        min-width: 0 !important;
        max-width: 100vw !important;
        padding-top: 0;
        gap: 0;
    }
    .sidebar .menu-btn,
    .sidebar .collapse-btn,
    .sidebar .theme-btn {
        font-size: 1rem;
        padding: 10px 8px;
        margin-bottom: 0;
        border-radius: 0;
        flex: 1 1 auto;
        justify-content: center;
        align-items: center;
        flex-direction: column; /* Stack icon and text vertically */
        display: flex;
    }
    .sidebar .menu-btn span,
    .sidebar .collapse-btn .theme-label {
        display: block !important;
        font-size: 0.85em;
        margin: 0;
        margin-top: 4px;
        text-align: center;
        opacity: 1 !important;
        width: 100%;
        pointer-events: none;
    }
    .sidebar .menu-btn i,
    .sidebar .collapse-btn i,
    .sidebar .theme-btn i {
        display: block;
        margin: 0 auto;
    }
    .sidebar .theme-btn .theme-label {
        display: block !important;
        font-size: 0.85em;
        margin-top: 4px;
        text-align: center;
    }
    .sidebar .collapse-btn span {
        display: block !important;
        font-size: 0.85em;
        margin-top: 4px;
        text-align: center;
    }
    .sidebar .menu-btn[aria-current="page"] {
        background: #fff;
        color: #2d3a4b;
        border-left: none;
        border-bottom: 4px solid var(--accent);
    }
    .main-content {
        margin-left: 0 !important;
        margin-top: 60px;
        padding: 16px 2vw 16px 2vw;
    }
    .sidebar ~ .main-content {
        margin-left: 0 !important;
    }
    .lobby-intro-columns {
        column-count: 1;
        padding: 1rem;
    }
    .stats-row {
        flex-direction: column;
        gap: 16px;
    }
}
/* ...existing code... */

@media (min-width: 576px) and (max-width: 767.98px) {
    .sidebar {
        width: 60px;
        min-width: 60px;
        max-width: 60px;
        padding-top: 16px;
    }
    .sidebar .menu-btn span {
        display: none !important;
    }
    .main-content {
        margin-left: 60px;
        padding: 24px 3vw 24px 3vw;
    }
    .lobby-intro-columns {
        column-count: 1;
        padding: 1.2rem;
    }
    .stats-row {
        flex-direction: column;
        gap: 20px;
    }
}

@media (min-width: 768px) and (max-width: 991.98px) {
    .sidebar {
        width: 80px;
        min-width: 80px;
        max-width: 80px;
        padding-top: 24px;
    }
    .sidebar .menu-btn span {
        display: none !important;
    }
    .main-content {
        margin-left: 80px;
        padding: 32px 4vw 32px 4vw;
    }
    .lobby-intro-columns {
        column-count: 1;
        padding: 1.5rem;
    }
}

@media (min-width: 992px) and (max-width: 1199.98px) {
    .sidebar {
        width: 180px;
        min-width: 180px;
        max-width: 180px;
        padding-top: 32px;
    }
    .sidebar .menu-btn span {
        display: inline-block !important;
    }
    .main-content {
        margin-left: 180px;
        padding: 36px 5vw 36px 5vw;
    }
    .lobby-intro-columns {
        column-count: 2;
        padding: 1.8rem;
    }
}

@media (min-width: 1200px) and (max-width: 1535.98px) {
    .sidebar {
        width: 220px;
        min-width: 220px;
        max-width: 220px;
        padding-top: 40px;
    }
    .main-content {
        margin-left: 220px;
        padding: 40px 6vw 40px 6vw;
    }
    .lobby-intro-columns {
        column-count: 2;
        padding: 2rem;
    }
}
@media (min-width: 1536px) and (max-width: 1919.98px) {
    .sidebar {
        width: 260px;
        min-width: 260px;
        max-width: 260px;
    }
    .main-content {
        margin-left: 260px;
        padding: 48px 8vw 48px 8vw;
    }
    .lobby-intro-columns {
        column-count: 3;
        padding: 2.2rem;
    }
}

@media (min-width: 1920px) {
    .sidebar {
        width: 320px;
        min-width: 320px;
        max-width: 320px;
    }
    .main-content {
        margin-left: 320px;
        padding: 60px 12vw 60px 12vw;
        max-width: 1800px;
        margin-right: auto;
        margin-left: 320px;
    }
    .lobby-intro-columns {
        column-count: 3;
        padding: 2.5rem;
    }
}
.comments-section,
.share-section,
.tab-content,
.stat-box,
.carousel,
.intro {
    max-width: 100vw;
    box-sizing: border-box;
    overflow-x: auto;
}
.comments-list li,
ul.resource-grid li {
    flex-direction: column;
    align-items: flex-start;
    gap: 4px;
    word-break: break-word;
}

.comment-form {
    display: flex;
    flex-direction: row;
    gap: 10px;
    align-items: stretch;
}
.comment-form input[type="text"] {
    flex: 0 0 90px;
    max-width: 90px;
    min-width: 60px;
    height: 40px;
    box-sizing: border-box;
}
.comment-form textarea {
    flex: 1 1 100%;
    min-width: 0;
    width: 100%;
    max-width: 100%;
    min-height: 40px;
    max-height: 40px;
    height: 40px;
    resize: none;
    overflow-y: auto;
    transition: height 0.2s;
    box-sizing: border-box;
    line-height: 1.4;
    padding-top: 8px;
    padding-bottom: 8px;
}
.comment-form button {
    height: 40px;
    box-sizing: border-box;
    display: flex;
    align-items: center;
    justify-content: center;
    white-space: nowrap;
    padding: 0 18px;
    font-size: 1rem;
    border-radius: 6px;
    background: #2d3a4b;
    color: #fff;
    border: none;
    cursor: pointer;
    transition: background 0.2s;
}

body.sidebar-collapsed .sidebar {
    width: var(--sidebar-collapsed) !important;
    min-width: var(--sidebar-collapsed) !important;
    max-width: var(--sidebar-collapsed) !important;
    padding-top: 20px !important;
    gap: 0.2rem !important;
}
body.sidebar-collapsed .main-content {
    margin-left: var(--sidebar-collapsed) !important;
}

.theme-btn {
    position: relative;
    margin: 0 0 20px 0;
    background: linear-gradient(135deg, #fff 0%, #e0e4ea 100%);
    color: #2d3a4b;
    border: none;
    border-radius: 50%;
    width: 48px;
    height: 48px;
    font-size: 2rem;
    box-shadow: 0 0 8px 2px #1abc9c55, 0 2px 8px #0002;
    transition: background 0.4s, color 0.4s, box-shadow 0.4s, transform 0.2s;
    outline: 3px solid #1abc9c;
    outline-offset: 2px;
    animation: theme-glow 2s infinite alternate;
    z-index: 1001;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
}
.theme-btn:hover, .theme-btn:focus {
    background: linear-gradient(135deg, #1abc9c 0%, #a259e6 100%);
    color: #fff;
    box-shadow: 0 0 32px 8px #a259e6aa, 0 2px 8px #0002;
    outline: 3px solid #a259e6;
}
@keyframes theme-glow {
    0% { box-shadow: 0 0 8px 2px #1abc9c55, 0 2px 8px #0002; }
    100% { box-shadow: 0 0 16px 4px #a259e6aa, 0 2px 8px #0002; }
}
.theme-btn::after {
    content: attr(data-tooltip);
    position: absolute;
    left: 110%;
    top: 50%;
    transform: translateY(-50%);
    background: #2d3a4b;
    color: #fff;
    padding: 6px 16px;
    border-radius: 8px;
    font-size: 1rem;
    opacity: 0;
    pointer-events: none;
    white-space: nowrap;
    transition: opacity 0.3s, left 0.3s;
    z-index: 1002;
}
.theme-btn:hover::after, .theme-btn:focus::after {
    opacity: 1;
    left: 120%;
}
body.dark-mode .theme-btn {
    background: linear-gradient(135deg, #2d3a4b 0%, #a259e6 100%);
    color: #fff;
    outline: 3px solid #a259e6;
    box-shadow: 0 0 24px 8px #a259e6aa, 0 2px 8px #0002;
}

body, .main-content {
    transition: background 0.7s cubic-bezier(.4,2,.6,1), color 0.7s cubic-bezier(.4,2,.6,1);
}
.sidebar:not(.collapsed) .theme-btn {
    width: 100%;
    min-width: 0;
    max-width: none;
    border-radius: 0 30px 30px 0;
    justify-content: flex-start;
    padding: 18px 30px;
    font-size: 1.1rem;
    background: linear-gradient(90deg, var(--accent), #fff 90%);
    color: #2d3a4b;
    transition: all 0.4s cubic-bezier(.4,2,.6,1);
    box-shadow: 0 2px 16px 2px var(--accent, #1abc9c33);
    outline: 3px solid var(--accent);
    align-items: center;
    gap: 12px;
    height: auto;
}
.sidebar:not(.collapsed) .theme-btn .theme-label {
    display: inline;
    margin-left: 16px;
    font-weight: 600;
    letter-spacing: 1px;
    color: inherit;
    transition: color 0.4s;
}
.sidebar.collapsed .theme-btn .theme-label {
    display: none;
}

.sidebar.collapsed .theme-btn {
    width: 48px;
    min-width: 48px;
    max-width: 48px;
    border-radius: 50%;
    justify-content: center;
    padding-left: 0;
    font-size: 2rem;
    background: var(--accent);
    color: #fff;
    outline: 3px solid #fff;
    box-shadow: 0 0 16px 4px var(--accent, #1abc9c55), 0 2px 8px #0002;
    transition: all 0.4s cubic-bezier(.4,2,.6,1);
}

body.dark-mode .sidebar:not(.collapsed) .theme-btn {
    background: linear-gradient(90deg, var(--accent-dark), #2d3a4b 90%);
    color: #fff;
    outline: 3px solid var(--accent-dark);
}
body.dark-mode .sidebar.collapsed .theme-btn {
    background: var(--accent-dark);
    color: #fff;
    outline: 3px solid #fff;
}

.dark-theme .authors,
.dark-theme .section-title,
.dark-theme .social-icon {
    color: #fff !important;
    fill: #fff !important;
}

body.dark-mode .authors-row .author,
body.dark-mode .section-title,
body.dark-mode .fa,
body.dark-mode .fa-solid,
body.dark-mode .fa-regular,
body.dark-mode .fa-brands,
body.dark-mode .fab,
body.dark-mode .fa-comments,
body.dark-mode .fa-share-nodes,
body.dark-mode .fa-house,
body.dark-mode .fa-square-root-variable,
body.dark-mode .fa-book,
body.dark-mode .fa-atom,
body.dark-mode .fa-flask,
body.dark-mode .fa-bullhorn,
body.dark-mode .fa-link {
    color: #fff !important;
    fill: #fff !important;
}
body.dark-mode .section-title {
    color: #fff !important;
}
body.dark-mode .thumb-btn span {
    color: #fff !important;
}

    </style>

</head>

<body>
    <nav class="sidebar" id="sidebar" aria-label="Meniu principal">
        <button class="collapse-btn" id="collapse-btn" title="Restrânge/Extinde bara laterală" aria-label="Restrânge/Extinde bara laterală"><i class="fa fa-angle-double-left"></i></button>
        <button class="theme-btn" id="theme-btn" title="Comută tema" aria-label="Comută tema"> <span id="theme-icon" style="display:inline-block;transition:transform 0.5s cubic-bezier(.4,2,.6,1);"> <i class="fa fa-moon"></i> </span> <span class="theme-label">Temă</span> </button>
        <button class="menu-btn active" data-instance="lobby" aria-current="page" title="Receptie" aria-label="Receptie"><i class="fa-solid fa-house"></i> <span>Receptie</span></button>
        <button class="menu-btn" data-instance="math" title="Matematică" aria-label="Matematică"><i class="fa-solid fa-square-root-variable"></i> <span>Matematică</span></button>
        <button class="menu-btn" data-instance="romanian" title="Română" aria-label="Română"><i class="fa-solid fa-book"></i> <span>Română</span></button>
        <button class="menu-btn" data-instance="physics" title="Fizică" aria-label="Fizică"><i class="fa-solid fa-atom"></i> <span>Fizică</span></button>
        <button class="menu-btn" data-instance="chemistry" title="Chimie" aria-label="Chimie"><i class="fa-solid fa-flask"></i> <span>Chimie</span></button>
        <button class="menu-btn" data-instance="news" title="Noutăți" aria-label="Noutăți"><i class="fa-solid fa-bullhorn"></i> <span>Noutăți</span></button>
        <button class="menu-btn" data-instance="mathlinks" title="Linkuri Matematică" aria-label="Linkuri Matematică"><i class="fa-solid fa-link"></i> <span>Linkuri Matematică</span></button>
        <button class="menu-btn" data-instance="romanianlinks" title="Linkuri Română" aria-label="Linkuri Română"><i class="fa-solid fa-link"></i> <span>Linkuri Română</span></button>
        <button class="menu-btn" data-instance="allcomments" title="Comentarii" aria-label="Comentarii"><i class="fa-solid fa-comments"></i> <span>Comentarii</span>
        </button>
    </nav>

    <div id="modal-root"></div>
    <button id="scrollTopBtn" class="scroll-top-btn" title="Sus"><i class="fa fa-arrow-up"></i></button>
    <main class="main-content" id="main-content" tabindex="0"></main>

    <script src="https://cdn.jsdelivr.net/npm/qrious@4.0.2/dist/qrious.min.js"></script>
    <script>

        const FORBIDDEN_WORDS = ['term1', 'term2', 'term3'];
function containsForbiddenWords(text) {
    let normalized = text.normalize('NFD').replace(/[\u0300-\u036f]/g, '').toLowerCase();

    return FORBIDDEN_WORDS.some(word => {
        if (!word) return false;
        const pattern = word
            .toLowerCase()
            .split('')
            .map(l => `.*${l}`)
            .join('') + '.*';
        const re = new RegExp(pattern, 'i');
        return re.test(normalized);
    });
}
       
       function $(sel) { return document.querySelector(sel); }
        function $$(sel) { return Array.from(document.querySelectorAll(sel)); }
        function escapeHTML(str) {
            return str.replace(/[&<>"']/g, m => ({
                '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'
            })[m]);
        }

        function getVisitorCount() {
            let count = parseInt(localStorage.getItem('Educatia de succes_visits') || '0', 10);
            count++;
            localStorage.setItem('Educatia de succes_visits', count);
            return count;
        }

        const mainContent = $('#main-content');
        const menuBtns = $$('.menu-btn');
        menuBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                $$('.menu-btn').forEach(b => b.classList.remove('active'));
                $$('.menu-btn').forEach(b => b.removeAttribute('aria-current'));
                btn.classList.add('active');
                btn.setAttribute('aria-current', 'page');
                loadInstance(btn.dataset.instance);
            });
        });

        const sidebar = $('#sidebar');
        const collapseBtn = $('#collapse-btn');
        function setSidebarCollapsed(collapsed) {
    if (collapsed) {
        sidebar.classList.add('collapsed');
        collapseBtn.innerHTML = '<i class="fa fa-angle-double-right"></i>';
        document.body.classList.add('sidebar-collapsed'); // <-- add this line
    } else {
        sidebar.classList.remove('collapsed');
        collapseBtn.innerHTML = '<i class="fa fa-angle-double-left"></i>';
        document.body.classList.remove('sidebar-collapsed'); // <-- add this line
    }
    localStorage.setItem('Educatia de succes_sidebar_collapsed', collapsed ? '1' : '0');
}
        collapseBtn.onclick = function() {
            setSidebarCollapsed(!sidebar.classList.contains('collapsed'));
        };
        setSidebarCollapsed(localStorage.getItem('Educatia de succes_sidebar_collapsed') === '1');

        const instances = {
            lobby: {
                title: 'Educatia de succes',
                authors: ['H. Rares', 'H. Bianca'],
                intro: `<b>Bine ați venit pe Educatia de succes!</b><br>Acest site reprezintă un reper academic de excelență, dedicat elevilor, studenților și tuturor celor pasionați de cunoaștere. Materialele prezentate sunt de cea mai înaltă calitate, elaborate cu rigurozitate științifică și actualizate constant pentru a răspunde cerințelor educaționale moderne. Site-ul nostru este destinat celor care aspiră la performanță, profesorilor care caută resurse valoroase și tuturor celor care apreciază educația autentică. Vă invităm să explorați conținutul și să contribuiți la dezvoltarea unei comunități academice solide!`,
                showComments: true,
                showShare: true,
                carousel: [
                    { text: "Resurse de matematică, fizică, chimie și limba română la cel mai înalt nivel.", icon: "fa-solid fa-graduation-cap" },
                    { text: "Comentarii și discuții deschise pentru toți utilizatorii.", icon: "fa-solid fa-comments" },
                    { text: "Distribuie rapid resursele preferate cu prietenii tăi!", icon: "fa-solid fa-share-nodes" }
                ],
                stats: true
            },

            math: {
                title: 'Matematică',
                authors: [],
                intro: `Secțiunea de matematică oferă resurse avansate pentru aprofundarea conceptelor fundamentale și aplicate. Materialele sunt structurate pentru a facilita înțelegerea și dezvoltarea gândirii logice.`,
                showComments: false,
                showShare: false,
                tabs: [
                    {
                        name: "Clasa a V-a",
                        content: `<b>Fracții, numere naturale, probleme de logică.</b>`
                    },
                    {
                        name: "Clasa a VI-a",
                        content: `<b>Proporții, ecuații simple, geometrie de bază.</b>`
                    },
                    {
                        name: "Clasa a VII-a",
                        content: `<b>Ecuații, inegalități, funcții elementare.</b>`
                    },
                    {
                        name: "Clasa a VIII-a",
                        content: `<b>Teorema lui Pitagora, funcții, sisteme de ecuații, recapitulare pentru Evaluarea Națională.</b>`
                    }
                ]
            },

            romanian: {
                title: 'Limba și literatura română',
                authors: [],
                intro: `Descoperiți universul literaturii române și al limbii, cu analize, comentarii și resurse pentru dezvoltarea abilităților lingvistice și interpretative.`,
                showComments: false,
                showShare: false,
                tabs: [
                    {
                        name: "Clasa a V-a",
                        content: `<b>Elemente de bază ale comunicării, părți de vorbire, texte narative.</b>`
                    },
                    {
                        name: "Clasa a VI-a",
                        content: `<b>Descrierea, dialogul, povestirea, analiza textului literar.</b>`
                    },
                    {
                        name: "Clasa a VII-a",
                        content: `<b>Argumentarea, textul dramatic, poezie, analiză literară.</b>`
                    },
                    {
                        name: "Clasa a VIII-a",
                        content: `<b>Recapitulare pentru Evaluarea Națională, eseuri, texte nonliterare.</b>`
                    }
                ]
            },

            physics: {
                title: 'Fizică',
                authors: [],
                intro: `Resurse pentru studiul fizicii: legi fundamentale, experimente, aplicații practice pentru clasele 5-8.`,
                showComments: false,
                showShare: false,
                tabs: [
                    {
                        name: "Clasa a V-a",
                        content: `<b>Noțiuni introductive, măsurători, unități de măsură.</b>`
                    },
                    {
                        name: "Clasa a VI-a",
                        content: `<b>Forțe, mișcare, energie.</b>`
                    },
                    {
                        name: "Clasa a VII-a",
                        content: `<b>Presiunea, densitatea, fenomene termice.</b>`
                    },
                    {
                        name: "Clasa a VIII-a",
                        content: `<b>Electricitate, magnetism, recapitulare pentru Evaluarea Națională.</b>`
                    }
                ]
            },

            chemistry: {
                title: 'Chimie',
                authors: [],
                intro: `Resurse pentru studiul chimiei: substanțe, reacții, experimente pentru clasele 5-8.`,
                showComments: false,
                showShare: false,
                tabs: [
                    {
                        name: "Clasa a V-a",
                        content: `<b>Introducere în chimie, materie și proprietăți.</b>`
                    },
                    {
                        name: "Clasa a VI-a",
                        content: `<b>Substanțe pure și amestecuri, separarea amestecurilor.</b>`
                    },
                    {
                        name: "Clasa a VII-a",
                        content: `<b>Structura atomului, reacții chimice simple.</b>`
                    },
                    {
                        name: "Clasa a VIII-a",
                        content: `<b>Acizi, baze, săruri, recapitulare pentru Evaluarea Națională.</b>`
                    }
                ]
            },
            allcomments: {
   
                title: 'Toate comentariile',
    
                authors: [],
   
                intro: `Aici poți vedea toate comentariile, poți reacționa și răspunde.`,
  
                showComments: false,
  
                showShare: false,
    
                customRender: true
},

    news: {
        title: 'Noutăți importante',
        authors: [],
        intro: `Aici puteți consulta cele mai importante noutăți video pentru comunitatea Educatia de succes.`,
        showComments: false,
        showShare: false,
        tabs: [
            {
                name: "Noutăți",
                content: `<ul id="news-list"></ul>`
            }
        ]
    },
    mathlinks: {
        title: 'Linkuri Matematică',
        authors: [],
        intro: `Consultați linkuri video utile pentru matematică.`,
        showComments: false,
        showShare: false,
        tabs: [
            {
                name: "Linkuri",
                content: `<ul class="resource-grid" id="math-links-list"></ul>`
            }
        ]
    },
    romanianlinks: {
        title: 'Linkuri Română',
        authors: [],
        intro: `Consultați linkuri video utile pentru limba română.`,
        showComments: false,
        showShare: false,
        tabs: [
            {
                name: "Linkuri",
                content: `<ul class="resource-grid" id="romanian-links-list"></ul>`
            }
        ]
    }
};

function renderAllCommentsSection() {
    let comments = getAllComments();
    comments = comments.sort((a, b) => new Date(b.date) - new Date(a.date));
    const firstFive = comments.slice(-5);
    let rest = comments.slice(5);
    let weighted = [];
    let sortedComments = comments;
    rest.forEach((c, i) => {
        const count = Math.max(1, (c.up || 0) + 1);
        for (let j = 0; j < count; j++) weighted.push({c, i});
    });

    for (let i = weighted.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [weighted[i], weighted[j]] = [weighted[j], weighted[i]];
    }
    let seen = new Set();
    let randomizedRest = [];
    weighted.forEach(({c, i}) => {
        if (!seen.has(i)) {
            randomizedRest.push(c);
            seen.add(i);
        }
    });

    function renderComment(c, i) {
        let originalIdx = getAllComments().findIndex(
        x => x.date === c.date && x.name === c.name && x.text === c.text
            );
        let replies = '';
        if (c.replies && c.replies.length) {
            replies = `<ul class="replies-list" style="margin-left:30px;margin-top:5px;">
                <li>
                    <div class="comment-content">
                        <b>${escapeHTML(c.replies[0].name)}</b>: ${escapeHTML(c.replies[0].text)}
                        <div style="font-size:0.85em;color:#888;">${c.replies[0].date||''}</div>
                    </div>
                </li>
            </ul>`;
            if (c.replies.length > 1) {
                replies += `<button class="show-all-replies-btn" data-idx="${i}" style="margin-left:30px;margin-top:4px;">Vezi toate raspunsurile(${c.replies.length})</button>`;
            }
        }
             return `
        <li data-idx="${originalIdx}" style="position:relative;">
            <div class="comment-content">
                <b>${escapeHTML(c.name)}</b>: ${escapeHTML(c.text)}
                <div style="font-size:0.9em;color:#888;">${c.date||''}</div>
                <div class="reactions" style="position:absolute;right:0;bottom:0;display:flex;gap:6px;">
                    <button class="thumb-btn thumb-up${c.selected==='up'?' selected':''}" title="Îmi place"><i class="fa-regular fa-thumbs-up"></i> <span>${c.up||0}</span></button>
                    <button class="thumb-btn thumb-down${c.selected==='down'?' selected':''}" title="Nu-mi place"><i class="fa-regular fa-thumbs-down"></i> <span>${c.down||0}</span></button>
                    <button class="reply-btn">Raspunde</button>
                </div>
                <div class="reply-box" style="display:none;margin-top:8px;">
                    <input type="text" class="reply-name-input" name="reply-name" placeholder="Nume" maxlength="20" style="margin-right:8px;max-width:90px;">
                    <input type="text" class="reply-input" name="reply-text" placeholder="Răspunde..." maxlength="6000" style="width:60%;">
                    <button class="send-reply-btn">Trimite</button>
                    <div class="reply-warning" style="display:none;color:#ff0033;font-weight:600;margin-top:8px;">
                        Răspunsul tău conține cuvinte interzise!
                    </div>
                </div>
                ${replies}
            </div>
        </li>`;
    }

        let html = `
<div class="comments-section">
    <div class="section-title">Toate comentariile</div>
    <ul class="comments-list" id="all-comments-list">
        ${firstFive.map(renderComment).join('')}
    </ul>
    <ul class="comments-list" id="all-comments-list-rest">
        ${randomizedRest.map(renderComment).join('')}
    </ul>
    <form class="comment-form" id="allcomments-form" autocomplete="off">
        <input type="text" id="allcomments-name" placeholder="Nume" maxlength="20" required aria-label="Nume">
        <div style="position:relative;flex:1;">
            <textarea id="allcomments-text" placeholder="Comentariul tău..." rows="2" maxlength="6000" required aria-label="Comentariu"></textarea>
            <div id="allcomments-text-highlighter" style="pointer-events:none;position:absolute;left:0;top:0;width:100%;height:100%;color:transparent;z-index:2;white-space:pre-wrap;word-break:break-word;"></div>
            <div id="allcomments-char-counter" style="position:absolute;left:6px;bottom:-22px;font-size:0.95em;color:#888;">0/6000</div>
        </div>
        <button type="submit">Trimite</button>
    </form>
    <div id="allcomments-forbidden-warning" style="display:none;color:#ff0033;font-weight:600;margin-top:32px;">
        Comentariul tău conține cuvinte jignitoare, discriminare sau cuvinte inadecvate
    </div>
</div>
`;
    mainContent.innerHTML = html;
    setupAllCommentsFormEvents();
    setupAllCommentsReactions();
}
function setupAllCommentsFormEvents() {
    const textarea = document.getElementById('allcomments-text');
    const counter = document.getElementById('allcomments-char-counter');
    const warning = document.getElementById('allcomments-forbidden-warning');
    if (!textarea || !counter) return;

    textarea.oninput = function() {
        counter.textContent = `${textarea.value.length}/6000`;
        highlightForbiddenWordsTextarea(textarea); // pentru highlight
        if (containsForbiddenWords(textarea.value)) {
            textarea.classList.add('forbidden');
            if (warning) warning.style.display = 'block';
        } else {
            textarea.classList.remove('forbidden');
            if (warning) warning.style.display = 'none';
        }
    };
    textarea.oninput();

    const form = document.getElementById('allcomments-form');
    if (form) {
        form.onsubmit = function(e) {
            e.preventDefault();
            const name = document.getElementById('allcomments-name').value.trim();
            const text = textarea.value.trim();
            if (!name || !text) return;
            if (containsForbiddenWords(text)) return;
            let comments = getAllComments();
            comments.push({
                name,
                text,
                date: new Date().toLocaleString(),
                up: 0,
                down: 0
            });
            localStorage.setItem('Educatia de succes_comments', JSON.stringify(comments));
            form.reset();
            renderAllCommentsSection();
            return false;
        };
    }
}
function setupAllCommentsReactions() {
    $$('.thumb-btn.thumb-up').forEach(btn => {
        btn.onclick = function(e) {
            e.preventDefault();
            let li = btn.closest('li[data-idx]');
            if (!li) return;
            let i = parseInt(li.getAttribute('data-idx'));
            let comments = getAllComments();
            let c = comments[i];
            if (!c) return;
            if (c.selected === 'up') {
                c.up = (c.up || 1) - 1;
                c.selected = undefined;
            } else {
                if (c.selected === 'down') c.down = (c.down || 1) - 1;
                c.up = (c.up || 0) + 1;
                c.selected = 'up';
            }
            localStorage.setItem('Educatia de succes_comments', JSON.stringify(comments));
            renderAllCommentsSection();
        };
    });
    $$('.thumb-btn.thumb-down').forEach(btn => {
        btn.onclick = function(e) {
            e.preventDefault();
            let li = btn.closest('li[data-idx]');
            if (!li) return;
            let i = parseInt(li.getAttribute('data-idx'));
            let comments = getAllComments();
            let c = comments[i];
            if (!c) return;
            if (c.selected === 'down') {
                c.down = (c.down || 1) - 1;
                c.selected = undefined;
            } else {
                if (c.selected === 'up') c.up = (c.up || 1) - 1;
                c.down = (c.down || 0) + 1;
                c.selected = 'down';
            }
            localStorage.setItem('Educatia de succes_comments', JSON.stringify(comments));
            renderAllCommentsSection();
        };
    });
}
setupAllCommentsReactions();


function renderAllCommentsSectionWith(comments) {
    let html = `
<div class="comments-section">
    <div class="section-title">Toate comentariile</div>
   <form class="comment-form" id="allcomments-form" autocomplete="off">
    <input type="text" id="allcomments-name" placeholder="Nume" maxlength="20" required aria-label="Nume">
    <div style="position:relative;flex:1;">
        <textarea id="allcomments-text" placeholder="Comentariul tău..." rows="2" maxlength="6000" required aria-label="Comentariu"></textarea>
        <div id="allcomments-text-highlighter" style="pointer-events:none;position:absolute;left:0;top:0;width:100%;height:100%;color:transparent;z-index:2;white-space:pre-wrap;word-break:break-word;"></div>
        <div id="allcomments-char-counter" style="position:absolute;left:6px;bottom:-22px;font-size:0.95em;color:#888;">0/6000</div>
    </div>
    <button type="submit">Trimite</button>
</form>
    <div id="allcomments-forbidden-warning" style="display:none;color:#ff0033;font-weight:600;margin-top:32px;">
        Comentariul tău conține cuvinte jignitoare, discriminare sau cuvinte inadecvate
    </div>
    <!-- Comentariile sunt jos, după formular -->
    <ul class="comments-list" id="all-comments-list">
        ${firstFive.map(renderComment).join('')}
    </ul>
    <ul class="comments-list" id="all-comments-list-rest">
        ${randomizedRest.map(renderComment).join('')}
    </ul>
</div>
`;
    mainContent.innerHTML = html;
    setupAllCommentsEvents();
}

               const YOUTUBE_LINKS = {
            news: [
                "https://www.youtube.com/watch?v=ysz5S6PUM-U",
                "https://youtu.be/dQw4w9WgXcQ",
                "https://www.youtube.com/watch?v=3JZ_D3ELwOQ",
                "https://www.youtube.com/watch?v=ScMzIvxBSi4",
                "https://www.youtube.com/watch?v=2Vv-BfVoq4g",
                "https://www.youtube.com/watch?v=5MgBikgcWnY"
            ],
            math: [
                "https://www.youtube.com/watch?v=H14bBuluwB8",
                "https://www.youtube.com/watch?v=2SUwOgmvz5A",
                "https://www.youtube.com/watch?v=V-_O7nl0Ii0",
                "https://www.youtube.com/watch?v=5MgBikgcWnY",
                "https://www.youtube.com/watch?v=ysz5S6PUM-U",
                "https://www.youtube.com/watch?v=3JZ_D3ELwOQ"
            ],
            romanian: [
                "https://www.youtube.com/watch?v=9bZkp7q19f0",
                "https://www.youtube.com/watch?v=3tmd-ClpJxA",
                "https://www.youtube.com/watch?v=OPf0YbXqDm0",
                "https://www.youtube.com/watch?v=ScMzIvxBSi4",
                "https://www.youtube.com/watch?v=ysz5S6PUM-U",
                "https://www.youtube.com/watch?v=2Vv-BfVoq4g"
            ]
        };
                const VIDEO_INFOS = {
            news: [
                "Prezentare generală a platformei educaționale.",
                "Motivație și perseverență în învățare.",
                "Strategii pentru succes academic.",
                "Importanța colaborării între elevi.",
                "Tehnici moderne de studiu.",
                "Noutate: Resurse video pentru toți."
            ],
            math: [
                "Matematică: Introducere în fracții.",
                "Geometrie: Bazele triunghiurilor.",
                "Matematică distractivă pentru toți.",
                "Cum să înveți eficient matematica.",
                "Exerciții de logică matematică.",
                "Recapitulare: formule esențiale."
            ],
            romanian: [
                "Limba română: Poezie și expresivitate.",
                "Analiză literară: Text narativ.",
                "Exerciții de gramatică pentru gimnaziu.",
                "Recapitulare: Figuri de stil.",
                "Tehnici de argumentare.",
                "Lectură suplimentară recomandată."
            ]
        };

        function renderCarousel(carousel) {
            if (!carousel || !carousel.length) return '';
            return `<div class="carousel" id="carousel">
                <div class="carousel-inner" id="carousel-inner">
                    ${carousel.map(c => `<div class="carousel-slide"><i class="${c.icon}" style="font-size:2.2rem;color:var(--accent);"></i><br>${c.text}</div>`).join('')}
                </div>
                <div class="carousel-controls">
                    <button class="carousel-btn" id="carousel-prev" aria-label="Anterior"><i class="fa fa-chevron-left"></i></button>
                    <button class="carousel-btn" id="carousel-next" aria-label="Următor"><i class="fa fa-chevron-right"></i></button>
                </div>
            </div>`;
        }

        function setupCarousel(carousel) {
            if (!carousel) return;
            let idx = 0;
            const slides = $('#carousel-inner').children.length;
            function update() {
                $('#carousel-inner').style.transform = `translateX(-${idx * 100}%)`;
            }
            $('#carousel-prev').onclick = () => { idx = (idx-1+slides)%slides; update(); };
            $('#carousel-next').onclick = () => { idx = (idx+1)%slides; update(); };
        }

        function renderTabs(tabs) {
            if (!tabs || !tabs.length) return '';
            return `<div class="tabs">${tabs.map((t,i)=>`<button class="tab-btn${i===0?' active':''}" data-tab="${i}" tabindex="0">${t.name}</button>`).join('')}</div>
            <div class="tab-content" id="tab-content">${tabs[0].content}</div>`;
        }

        function setupTabs(tabs, key) {
            if (!tabs) return;
            $$('.tab-btn').forEach(btn => {
                btn.onclick = function() {
                    $$('.tab-btn').forEach(b=>b.classList.remove('active'));
                    btn.classList.add('active');
                    $('#tab-content').innerHTML = tabs[btn.dataset.tab].content;
                    if (key === 'news') setupNewsLinks();
                    if (key === 'mathlinks') setupMathLinks();
                    if (key === 'romanianlinks') setupRomanianLinks();
                };
                btn.onkeydown = e => { if (e.key === 'Enter') btn.click(); };
            });
            if (key === 'news') setupNewsLinks();
            if (key === 'mathlinks') setupMathLinks();
            if (key === 'romanianlinks') setupRomanianLinks();
        }

        function loadInstance(key) {
    const inst = instances[key];
    // Secțiune specială pentru allcomments
    if (key === 'allcomments') {
        renderAllCommentsSection();
        return;
    }
    let html = '';
    html += `<div class="lobby-title" aria-label="${inst.title}">${inst.title}</div>`;
    if (inst.authors && inst.authors.length) {
        html += `<div class="authors-row"><div class="author">${inst.authors[0]||''}</div><div></div><div class="author">${inst.authors[1]||''}</div></div>`;
    }
    if (inst.carousel) html += renderCarousel(inst.carousel);
    html += inst.intro ? `<div class="intro">${inst.intro}</div>` : '';
    if (inst.tabs) html += renderTabs(inst.tabs, key);
    if (inst.showComments) html += renderCommentsSection();
    if (inst.showShare) html += renderShareSection();
    mainContent.innerHTML = html;
    if (inst.carousel) setupCarousel(inst.carousel);
    if (inst.tabs) setupTabs(inst.tabs, key);
    if (inst.showComments) loadComments();
    if (inst.showShare) setupShare();
    if (key === 'lobby') showStatsBelowComments();
}

    function renderCommentsSection() {
    return `<div class="comments-section">
        <div class="section-title">Comentarii</div>
        <ul class="comments-list" id="comments-list"></ul>
        <form class="comment-form" id="comment-form" autocomplete="off">
            <input type="text" id="comment-name" placeholder="Nume" maxlength="20" required aria-label="Nume">
            <div style="position:relative;flex:1;">
                <textarea id="comment-text" placeholder="Comentariul tău..." rows="2" maxlength="6000" required aria-label="Comentariu"></textarea>
                <div id="comment-text-highlighter" style="pointer-events:none;position:absolute;left:0;top:0;width:100%;height:100%;color:transparent;z-index:2;white-space:pre-wrap;word-break:break-word;"></div>
                <div id="char-counter" style="position:absolute;left:6px;bottom:-22px;font-size:0.95em;color:#888;">0/6000</div>
            </div>
            <button type="submit">Trimite</button>
        </form>
        <div id="forbidden-warning" style="display:none;color:#ff0033;font-weight:600;margin-top:32px;">
            Comentariul tău conține cuvinte jignitoare, discriminare sau cuvinte inadecvate
        </div>
    </div>`;
}

        function getAllComments() {
            return JSON.parse(localStorage.getItem('Educatia de succes_comments') || '[]');
        }

function loadComments(limit = 5, showMoreBtn = true) {
    const list = $('#comments-list');
    let comments = getAllComments();
    comments = comments.sort((a, b) => new Date(b.date) - new Date(a.date));
    let shown = comments.slice(0, limit);
    list.innerHTML = shown.map((c,i) => {
        return `<li>
            <div class="comment-content">
                <b>${escapeHTML(c.name)}</b>: ${escapeHTML(c.text)}
                <div style="font-size:0.9em;color:#888;">${c.date||''}</div>
            </div>
        </li>`;
    }).join('');
    let oldBtnWrap = document.getElementById('see-more-btn-wrap');
    if (oldBtnWrap) oldBtnWrap.remove();
    if (showMoreBtn && comments.length > limit) {
        let btnWrap = document.createElement('div');
        btnWrap.id = 'see-more-btn-wrap';
        btnWrap.style.marginTop = '18px';
        btnWrap.style.display = 'flex';
        btnWrap.style.justifyContent = 'flex-start';
        let btn = document.createElement('button');
        btn.className = 'see-more-btn';
        btn.innerHTML = '<i class="fa fa-plus" style="margin-right:8px;"></i>Vezi mai multe';
        btn.onclick = () => {
            $$('.menu-btn').forEach(b => b.classList.remove('active'));
            $$('.menu-btn').forEach(b => b.removeAttribute('aria-current'));
            const commentsBtn = document.querySelector('.menu-btn[data-instance="allcomments"]');
            if (commentsBtn) {
                commentsBtn.classList.add('active');
                commentsBtn.setAttribute('aria-current', 'page');
            }
            loadInstance('allcomments');
        };
        btnWrap.appendChild(btn);
        list.parentNode.appendChild(btnWrap);
    }
}

function renderShareSection() {
            return `<div class="share-section">
                <div class="section-title">Distribuie</div>
                <button class="copy-link-btn" id="copy-link-btn">Copiază link-ul</button>
                <button class="copy-link-btn" id="email-share-btn"><i class="fa fa-envelope"></i> Email</button>
                <button class="qr-btn" id="qr-btn"><i class="fa fa-qrcode"></i> QR</button>
                <div class="share-icons">
                    <i class="fab fa-whatsapp" title="WhatsApp" data-share="whatsapp" tabindex="0"></i>
                    <i class="fab fa-facebook" title="Facebook" data-share="facebook" tabindex="0"></i>
                    <i class="fab fa-instagram" title="Instagram" data-share="instagram" tabindex="0"></i>
                    <i class="fab fa-telegram" title="Telegram" data-share="telegram" tabindex="0"></i>
                    <i class="fab fa-tiktok" title="TikTok" data-share="tiktok" tabindex="0"></i>
                </div>
            </div>`;
        }

        function setupShare() {
            $('#copy-link-btn').onclick = function() {
                navigator.clipboard.writeText(window.location.href);
                this.textContent = 'Copiat!';
                setTimeout(() => this.textContent = 'Copiază link-ul', 1200);
            };
            $('#email-share-btn').onclick = function() {
                window.location.href = `mailto:?subject=Educatia de succes&body=${encodeURIComponent(window.location.href)}`;
            };
            $('#qr-btn').onclick = function() {
                showModal(`<div class="qr-modal-content"><canvas id="qr-code-canvas"></canvas><br><button class="close-modal" onclick="closeModal()">Închide</button></div>`);
                setTimeout(() => {
                    new QRious({
                        element: $('#qr-code-canvas'),
                        value: window.location.href,
                        size: 180
                    });
                }, 100);
            };
            $$('.share-icons i').forEach(icon => {
                icon.onclick = function() {
                    const url = encodeURIComponent(window.location.href);
                    let shareUrl = '';
                    switch (this.dataset.share) {
                        case 'whatsapp':
                            shareUrl = `https://wa.me/?text=${url}`; break;
                        case 'facebook':
                            shareUrl = `https://www.facebook.com/sharer/sharer.php?u=${url}`; break;
                        case 'instagram':
                            alert('Instagram nu permite partajarea directă a link-urilor. Copiați link-ul și distribuiți manual.'); return;
                        case 'telegram':
                            shareUrl = `https://t.me/share/url?url=${url}`; break;
                        case 'tiktok':
                            alert('TikTok nu permite partajarea directă a link-urilor. Copiați link-ul și distribuiți manual.'); return;
                    }
                    if (shareUrl) window.open(shareUrl, '_blank');
                };
            });
        }

        function showModal(html) {
            const root = $('#modal-root');
            root.innerHTML = `<div class="modal-bg" tabindex="-1"><div class="modal" role="dialog" aria-modal="true">${html}</div></div>`;
            root.querySelector('.modal-bg').onclick = e => { if (e.target === root.querySelector('.modal-bg')) closeModal(); };
            root.querySelector('.close-modal')?.addEventListener('click', closeModal);
            setTimeout(() => { root.querySelector('button,canvas')?.focus(); }, 100);
            document.body.style.overflow = 'hidden';
        }
        function closeModal() {
            $('#modal-root').innerHTML = '';
            document.body.style.overflow = '';
        }

        function getYoutubeId(url) {
            const regExp = /(?:youtube\.com\/(?:[^\/]+\/.+\/|(?:v|e(?:mbed)?|shorts)\/|.*[?&]v=)|youtu\.be\/)([A-Za-z0-9_-]{11})/;
            const match = url.match(regExp);
            return match ? match[1] : null;
        }

       function renderYoutubeLinks(links, infos) {
            if (!links.length) return '<li><i>Niciun link adăugat.</i></li>';
            return links.map((l, i) => {
            return `<li style="margin-bottom:1em;">
            <a href="${escapeHTML(l)}" target="_blank">Link ${i+1}</a>
            <div class="video-info">${escapeHTML(infos && infos[i] ? infos[i] : '')}</div>
        </li>`;
    }).join('');
}

        function setupNewsLinks() {
    const list = $('#news-list');
    let links = YOUTUBE_LINKS.news;
    let infos = VIDEO_INFOS.news || [];
    list.className = '';
    list.innerHTML = renderYoutubeLinks(links, infos);
}

function setupMathLinks() {
    const list = $('#math-links-list');
    let links = YOUTUBE_LINKS.math;
    let infos = VIDEO_INFOS.math || [];
    list.className = '';
    list.innerHTML = renderYoutubeLinks(links, infos);
}

function setupRomanianLinks() {
    const list = $('#romanian-links-list');
    let links = YOUTUBE_LINKS.romanian;
    let infos = VIDEO_INFOS.romanian || [];
    list.className = '';
    list.innerHTML = renderYoutubeLinks(links, infos);
}

function setupCommentFormEvents() {
    const textarea = document.getElementById('comment-text');
    const counter = document.getElementById('char-counter');
    const warning = document.getElementById('forbidden-warning');
    if (!textarea || !counter) return;

    textarea.oninput = function() {
        counter.textContent = `${textarea.value.length}/6000`;
        highlightForbiddenWordsTextarea(textarea);
        if (containsForbiddenWords(textarea.value)) {
            textarea.classList.add('forbidden');
            if (warning) warning.style.display = 'block';
        } else {
            textarea.classList.remove('forbidden');
            if (warning) warning.style.display = 'none';
        }
    };
    textarea.oninput();

    const form = document.getElementById('comment-form');
    if (form) {
        form.onsubmit = function(e) {
            e.preventDefault();
            const name = document.getElementById('comment-name').value.trim();
            const text = textarea.value.trim();
            if (!name || !text) return;
            if (containsForbiddenWords(text)) return;
            let comments = getAllComments();
            comments.push({
                name,
                text,
                date: new Date().toLocaleString(),
                up: 0,
                down: 0
            });
            localStorage.setItem('Educatia de succes_comments', JSON.stringify(comments));
            form.reset();
            loadComments();
            return false;
        };
    }
}


function showStatsBelowComments() {
    const visits = getVisitorCount();
    const comments = getAllComments().length;
    const section = document.createElement('div');
    section.style.margin = "1.5rem 0 0 0";
    section.innerHTML = `<div style="font-size:1.1rem;"><b>Persoane vizitate:</b> ${visits} &nbsp; | &nbsp; <b>Comentarii:</b> ${comments}</div>`;
    const commentsSection = document.querySelector('.comments-section');
    if (commentsSection) commentsSection.parentNode.insertBefore(section, commentsSection.nextSibling);
}
        loadInstance('lobby');

        $$('.menu-btn, .collapse-btn').forEach(btn => {
            btn.onkeydown = e => { if (e.key === 'Enter') btn.click(); };
        });

        mainContent.onkeydown = e => {
            if (e.key === 'Tab') mainContent.focus();
        };

        const scrollTopBtn = document.getElementById('scrollTopBtn');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 200) {
                scrollTopBtn.style.display = 'block';
            } else {
                scrollTopBtn.style.display = 'none';
            }
        });
        scrollTopBtn.onclick = () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        };


const themeBtn = document.getElementById('theme-btn');
const themeIcon = document.getElementById('theme-icon');
function setTheme(dark) {
    const themeLabel = document.querySelector('.theme-label');
    if (dark) {
        document.body.classList.add('dark-mode');
        themeIcon.innerHTML = '<i class="fa fa-sun"></i>';
        themeIcon.style.transform = 'rotate(360deg) scale(1.2)';
        setTimeout(() => { themeIcon.style.transform = 'rotate(0deg) scale(1)'; }, 400);
        document.documentElement.style.setProperty('--accent', '#a259e6');
        document.documentElement.style.setProperty('--section-border', '2px solid #a259e6');
        if (themeLabel) themeLabel.textContent = 'Temă luminoasă';
        localStorage.setItem('Educatia de succes_theme', 'dark');
    } else {
        document.body.classList.remove('dark-mode');
        themeIcon.innerHTML = '<i class="fa fa-moon"></i>';
        themeIcon.style.transform = 'rotate(-360deg) scale(1.2)';
        setTimeout(() => { themeIcon.style.transform = 'rotate(0deg) scale(1)'; }, 400);
        document.documentElement.style.setProperty('--accent', '#1abc9c');
        document.documentElement.style.setProperty('--section-border', '2px solid #1abc9c');
        if (themeLabel) themeLabel.textContent = 'Temă întunecată';
        localStorage.setItem('Educatia de succes_theme', 'light');
    }
}
themeBtn.onclick = function() {
    setTheme(!document.body.classList.contains('dark-mode'));
};
setTheme(localStorage.getItem('Educatia de succes_theme') === 'dark');


function highlightForbiddenWordsTextarea(input) {
    let value = input.value;
    let html = escapeHTML(value);

    FORBIDDEN_WORDS.forEach(word => {
        if (!word) return;
        const pattern = word
            .split('')
            .map(l => escapeRegExp(l) + '(.*?)')
            .join('');
        const re = new RegExp(pattern, 'gi');
        html = html.replace(re, match =>
            `<span class="forbidden-highlight">${match}</span>`
        );
    });

    const highlighter = document.getElementById('comment-text-highlighter');
    if (highlighter) {
        highlighter.innerHTML = html + '<br>';
        highlighter.style.display = containsForbiddenWords(value) ? 'block' : 'none';
    }
}
function escapeRegExp(string) {
    return string.replace(/[.*+?^${}()|[\]\\]/g, '\\$&');
}

function showAllRepliesPage(commentIdx) {
    let comments = getAllComments();
    let c = comments[commentIdx];
    let html = `
        <div class="comments-section">
            <button class="back-to-comments-btn" style="margin-bottom:18px;">&larr; Înapoi la comentarii</button>
            <div class="section-title">Reply-uri pentru: <b>${escapeHTML(c.name)}</b></div>
            <div style="margin-bottom:1em;">${escapeHTML(c.text)}</div>
            <ul class="comments-list">
                ${c.replies.map(r => `
                    <li>
                        <div class="comment-content">
                            <b>${escapeHTML(r.name)}</b>: ${escapeHTML(r.text)}
                            <div style="font-size:0.85em;color:#888;">${r.date||''}</div>
                        </div>
                    </li>
                `).join('')}
            </ul>
        </div>
    `;
    mainContent.innerHTML = html;
    $('.back-to-comments-btn').onclick = function() {
        renderAllCommentsSection();
        setTimeout(() => {
            const target = document.querySelector(`[data-idx="${commentIdx}"]`);
            if (target) target.scrollIntoView({behavior:'smooth', block:'center'});
        }, 100);
    };
}

</script>
</body>
</html>
