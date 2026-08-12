Option B texture pack (ambientCG, CC0)

Place these in your project:
  public/textures/walnut_floor.jpg
  public/textures/reclaimed_siding.jpg
  public/textures/paper_grain.png

Suggested usage:
- Shelves/wood sections: walnut_floor.jpg or reclaimed_siding.jpg with a dark overlay.
- Page background: paper_grain.png at low opacity.

Example CSS:
  .shelf {
    background-image:
      linear-gradient(rgba(16,34,60,.35), rgba(16,34,60,.35)),
      url('/textures/walnut_floor.jpg');
    background-size: 900px auto;
    background-repeat: repeat;
  }

  body {
    background-color: #F6F2E9;
    background-image: url('/textures/paper_grain.png');
    background-size: 700px auto;
    background-repeat: repeat;
  }
