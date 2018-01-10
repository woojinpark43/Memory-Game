<script>
    let hiddenTiles = document.querySelectorAll("#hidden > div");
    let visibleTiles = document.querySelectorAll("#visible > div");

    let clickTile1 = null;
    let clickTile1Text = null;
    let clickTile2 = null;
    let clickTile2Text = null;

    for (let i = 0; i < hiddenTiles.length; i++) {
        let hidden = hiddenTiles[i];
        let visible = visibleTiles[i];
      
        visible.onclick = function() {
            if (visible.style.opacity !== "0") {
                //Flip incorrect tiles back over
                if (clickTile1Text !== null && clickTile2Text !== null) {
                    if (clickTile1Text !== clickTile2Text) {
                        clickTile1.style.opacity = 1;
                        clickTile2.style.opacity = 1;
                    }
                    clickTile1 = null;
                    clickTile1Text = null;
                    clickTile2 = null;
                    clickTile2Text = null;
                }
                 
                //Add current tile to be checked next time
                if (clickTile1 === null) {
                    clickTile1 = visible;
                    clickTile1Text = hidden.textContent;
                } else if (clickTile2 === null) {
                    clickTile2 = visible;
                    clickTile2Text = hidden.textContent;
                }
                visible.style.opacity = 0;
            }
        };
    }
</script>
