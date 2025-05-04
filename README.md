# Menu-Website

<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>EFAH Restoran Menüsü</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f9f9f9;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #d35400;
      color: white;
      padding: 20px;
      text-align: center;
      font-size: 34px;
      font-weight: bold;
      letter-spacing: 2px;
    }
    #menu-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin: 30px auto;
      max-width: 1200px;
    }
    .menu-item {
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      margin: 15px;
      overflow: hidden;
      width: 260px;
      transition: transform 0.3s;
    }
    .menu-item:hover {
      transform: scale(1.05);
    }
    .menu-item img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    .menu-content {
      padding: 15px;
    }
    .menu-content h2 {
      font-size: 22px;
      margin-bottom: 8px;
      color: #333;
    }
    .menu-content p {
      font-size: 15px;
      color: #666;
      margin-bottom: 6px;
    }
    .price {
      font-weight: bold;
      color: #222;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <header>EFAH Restoran Menüsü</header>

  <div id="menu-container"></div>

  <script>
    const menuItems = [
      { 
        name: "Pizza Margherita", 
        description: "Mozzarella, domates ve fesleğen ile hazırlanır.", 
        price: "340 TL", 
        image: "https://cdn.pixabay.com/photo/2017/12/09/08/18/pizza-3007395_960_720.jpg"
      },
      { 
        name: "Cheeseburger", 
        description: "Özel soslu, bol peynirli ev yapımı burger.", 
        price: "550 TL", 
        image: "https://cdn.pixabay.com/photo/2016/03/05/19/02/hamburger-1238246_960_720.jpg"
      },
      { 
        name: "Tavuklu Makarna", 
        description: "Kremalı sos ile tavuk parçalı makarna.", 
        price: "360 TL", 
        image: "file:///C:/Users/ataha/OneDrive/Masa%C3%BCst%C3%BC/kremasiz-korili-tavuklu-makarna.webp"
      },
      { 
        name: "Akdeniz Salatası", 
        description: "Taze yeşillikler, domates, salatalık ve zeytin.", 
        price: "90 TL", 
        image: "file:///C:/Users/ataha/OneDrive/Masa%C3%BCst%C3%BC/beyaz-peynirli-akdeniz-salatasi.webp"
      },
      { 
        name: "Adana Kebap", 
        description: "Adana, Urfa, tavuk şiş ve pirzola.", 
        price: "700 TL", 
        image: "file:///C:/Users/ataha/OneDrive/Masa%C3%BCst%C3%BC/adana-kebapsebze-esliginde.webp"
      },
      { 
        name: "Izgara Somon", 
        description: "Limon soslu ızgara somon fileto.", 
        price: "440 TL", 
        image: "file:///C:/Users/ataha/OneDrive/Masa%C3%BCst%C3%BC/sar-pisir-somon-tarifi-17.webp"
      },
      { 
        name: "Mantı", 
        description: "Geleneksel yoğurtlu ve soslu Türk mantısı.", 
        price: "300 TL", 
        image: "file:///C:/Users/ataha/OneDrive/Masa%C3%BCst%C3%BC/hazir-manti-nasil-yapilir-5.webp"
      },
      { 
        name: "Künefe", 
        description: "İçinde peynir olan sıcak şerbetli tatlı.", 
        price: "200 TL", 
        image: "file:///C:/Users/ataha/OneDrive/Masa%C3%BCst%C3%BC/kunefe-tarifi.webp"
      },
      { 
        name: "Çıtır Tavuk", 
        description: "Baharatlı çıtır kaplamalı tavuk parçaları.", 
        price: "300 TL", 
        image: "file:///C:/Users/ataha/OneDrive/Masa%C3%BCst%C3%BC/citir-tavuk-baget-1.webp"
      }
    ];

    const container = document.getElementById("menu-container");

    menuItems.forEach(item => {
      const div = document.createElement("div");
      div.className = "menu-item";
      div.innerHTML = `
        <img src="${item.image}" alt="${item.name}">
        <div class="menu-content">
          <h2>${item.name}</h2>
          <p>${item.description}</p>
          <div class="price">${item.price}</div>
        </div>
      `;
      container.appendChild(div);
    });
  </script>
</body>
</html>
