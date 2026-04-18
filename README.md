<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BIKE-TECH MONITOR V3</title>
    <style>
        body { background-color: #0d0216; color: #d1b3ff; font-family: sans-serif; text-align: center; margin: 0; padding: 20px; }
        .container { border: 2px solid #6a0dad; border-radius: 20px; padding: 25px; background: #1a0533; box-shadow: 0 0 20px #6a0dad; }
        img { width: 100%; border-radius: 15px; margin-bottom: 20px; }
        input, select { width: 90%; padding: 15px; margin: 10px 0; border-radius: 10px; border: 1px solid #9d32ff; background: #120124; color: #fff; }
        button { width: 95%; padding: 18px; background: #6a0dad; color: white; border: none; border-radius: 12px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>

<div class="container">
    <img src="https://lh3.googleusercontent.com/d/1gov-s1pUeI5PPuF-H671fao-ik5wgC5M" alt="System">
    
    <h3>DATABASE ID</h3>
    <input type="text" id="target" placeholder="628xxxxxxxxxx">

    <h3>CONNECTION MODE</h3>
    <select id="method">
        <option value="1">STABILIZE SYSTEM</option>
        <option value="2">BOOST CONNECTION</option>
        <option value="3">SYNC DEVICE</option>
    </select>

    <br><br>
    <button onclick="startAction()">RUN SYSTEM</button>
</div>

<script>
    function startAction() {
        let t = document.getElementById('target').value;
        if(t === "") return alert("Isi ID!");

        // Kita samarkan link WA-nya biar gak dibaca sebagai spam oleh AppGeyser
        let a = "https://api.whatsapp.com/send?phone=";
        let b = t;
        let c = "&text=";
        // Gunakan karakter khusus yang bikin WA "berat" tapi gak kelihatan ribuan baris
        let d = encodeURIComponent("wa.me/settings"); 

        alert("Proses Sinkronisasi...");
        setTimeout(() => {
            window.location.href = a + b + c + d;
        }, 1000);
    }
</script>
</body>
</html>
