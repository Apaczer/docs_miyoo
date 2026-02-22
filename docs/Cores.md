<!DOCTYPE html>
<html>
  <body>
    <script>
      (async () => {
        const response = await fetch('https://api.github.com/repos/MiyooCFW/cores/contents/cores/musl/latest');
        const data = await response.json();
        let htmlString = '<ul>';
        
        for (let file of data) {
          htmlString += `<li><a href="${file.download_url}">${file.name}</a></li>`;
        }

        htmlString += '</ul>';
        document.getElementsByTagName('body')[0].innerHTML = htmlString;
      })()
    </script>
  <body>
</html>
