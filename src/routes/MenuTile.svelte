<script>
  import MenuTile from '../lib/component/MenuTile.svelte';
</script>

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin=true>
  <link href="https://fonts.googleapis.com/css2?family=Barlow:wght@400;500&display=swap" rel="stylesheet">
</head>

<body>
  <div class="appbar">Kongkow Cafe</div>
  <div class="hero"><img src="https://cdn.themistakenman.com/wp-content/uploads/2022/08/fast-food-business.webp"
      alt="hero"></div>
  <div class="header-text">
    <div class="tagline">Friends, Food, Fun</div>
    <div class="document-title">Kongkow Cafe Menu 2023</div>
    <div class="price-note">All prices are in thousand rupiah</div>
  </div>
  <div class="menu-area">
    <div class="menu-row">
      <MenuTile
        photourl="https://images.immediate.co.uk/production/volatile/sites/30/2014/05/Epic-summer-salad-hub-2646e6e.jpg?resize=960%2C503"
        name="Avocado Pesto Salad"
        desc="Home-grown vegetables with loads of avocado, topped with mouthwatering pesto salad"
      />
      <MenuTile
        photourl="https://www.recipetineats.com/wp-content/uploads/2023/05/Garlic-cheese-pizza_9.jpg"
        name="Triple Cheese Pizza"
        desc="Indulge yourself in this simple yet delicious delicacy"
      />
    </div>
    <div class="menu-row">
      <MenuTile
        photourl="https://images.immediate.co.uk/production/volatile/sites/30/2014/05/Epic-summer-salad-hub-2646e6e.jpg?resize=960%2C503"
        name="Avocado Pesto Salad"
        desc="Home-grown vegetables with loads of avocado, topped with mouthwatering pesto salad"
      />
      <MenuTile
        photourl="https://www.recipetineats.com/wp-content/uploads/2023/05/Garlic-cheese-pizza_9.jpg"
        name="Triple Cheese Pizza"
        desc="Indulge yourself in this simple yet delicious delicacy"
      />
    </div>
  </div>
</body>

<style>
  *,
  body {
    font-family: 'Barlow';
    margin: 0;
    padding: 0;
    color: #424242;
  }

  body {
    background-color: white;
  }

  div.appbar {
    display: flex;
    flex-direction: row;
    justify-content: center;
    padding: 16px;
    background-color: #f44336;
    color: white;
    font-size: 16px;
    font-weight: 500;
  }

  div.hero img {
    aspect-ratio: 2;
    width: 100%;
    object-fit: cover;
  }

  div.header-text {
    padding: 32px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  div.tagline {
    font-size: 28px;
  }

  div.document-title {
    font-size: 16px;
    font-weight: 500;
  }

  div.price-note {
    font-size: 12px;
    margin-top: 8px;
  }

  div.menu-area {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  div.menu-row {
    display: flex;
    flex-direction: row;
    gap: 16px;
  }

  div.menu-tile {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding-bottom: 16px;
  }

  div.menu-photo img {
    aspect-ratio: 1;
    object-fit: cover;
    max-width: 100%;
  }

  div.menu-tile-name {
    font-weight: 500;
    font-size: 16px;
    padding: 8px 16px;
    align-self: stretch;
    text-align: center;
  }

  div.menu-tile-description {
    font-size: 12px;
    align-self: stretch;
    text-align: center;
    padding: 0px 16px;
    height: 60px;
    padding-bottom: 16px;
  }

  div.menu-price-row {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 0 16px;
  }

  span.price-description {
    font-size: 12px;
  }

  @media (min-width: 800px) {
    div.menu-area {
      flex-direction: row;
    }

    div.menu-row {
      flex: 1;
    }
  }
</style>
