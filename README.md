# altair-vega
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Altair &amp; Vega</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
  html { scroll-behavior: smooth; }
  body {
    background: #05060f;
    color: #e8e8f0;
    font-family: Georgia, 'Times New Roman', serif;
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
  }
  #stars {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    z-index: 0; pointer-events: none;
  }
  #sky {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    z-index: 1; pointer-events: none;
    background: radial-gradient(ellipse at 50% 30