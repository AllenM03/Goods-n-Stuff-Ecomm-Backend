mysql -u root -p
source db/schema.sql

npm run seed
npm start

Insomnia demonstrates

<!-- START WITH GET ROUTES  -->

http://localhost:3001/api/categories
http://localhost:3001/api/categories/2
http://localhost:3001/api/products
http://localhost:3001/api/products/1
http://localhost:3001/api/tags
http://localhost:3001/api/tags/1

<!-- ///////////////////////////////////////// -->



<!-- POST ROUTES -->

http://localhost:3001/api/categories

<!-- JSON -->
{
    "category_name": "jeans"
}



http://localhost:3001/api/products

<!-- JSON -->
{
    "product_name": "Jimi Hendrix tshirt",
    "price": "30.00",
    "stock": "18",
    "tagIds": [1,2,3,4,5]
}


http://localhost:3001/api/tags

<!-- JSON -->
{
    "tag_name": "lime"
}

<!-- /////////////////////////////////////////// -->



<!-- PUT ROUTES -->

http://localhost:3001/api/tags/1

<!-- JSON -->
{
    "tag_name": "Dub Reggae music"
}


http://localhost:3001/api/categories/3

<!-- JSON -->
{
    "category_name": "Graphic art shirts"
}

http://localhost:3001/api/products/2

<!-- JSON -->
{
    "product_name": "King Tubby shirts"
}

<!-- /////////////////////////////////////////// -->

<!-- DELETE ROUTES -->

http://localhost:3001/api/products/2

<!-- SET FROM JSON TO BODY -->

http://localhost:3001/api/products/2
<!-- SEND -->
http://localhost:3001/api/tags/1
<!-- SEND -->
http://localhost:3001/api/categories/3
<!-- SEND -->