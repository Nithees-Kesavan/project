


A complete full-stack e-commerce cart system built with Node.js backend and vanilla JavaScript frontend.


- ✅ Responsive product catalog with search
- ✅ Interactive shopping cart with real-time updates
- ✅ Promo code system with multiple discount types
- ✅ Complete checkout process with form validation
- ✅ Admin panel for product management
- ✅ Toast notifications for user feedback
- ✅ Local storage backup for offline functionality


- ✅ RESTful API with Express.js
- ✅ In-memory data storage (easily switchable to MongoDB)
- ✅ Session-based cart management
- ✅ Order processing and tracking
- ✅ Product management (CRUD operations)
- ✅ Promo code validation and application
- ✅ Security middleware (Helmet, Rate Limiting)
- ✅ Error handling and logging
- ✅ Health check endpoints


**Frontend:**
- HTML5, CSS3, JavaScript (ES6+)
- Font Awesome icons
- Unsplash images

**Backend:**
- Node.js with Express.js
- Body-parser for request handling
- CORS for cross-origin requests
- Helmet for security headers
- Express-rate-limit for API protection
- Morgan for logging
- UUID for unique ID generation

**Development:**
- Nodemon for auto-restart
- Jest for testing (configured)
- Docker support for deployment


```bash

npm install


npm run dev


npm start
```

```bash

./start-dev.sh


./start-prod.sh
```


```bash

docker-compose up --build


docker build -t ecommerce-cart .
docker run -p 3000:3000 ecommerce-cart
```


- `GET /api/products` - Get all products (with search & category filters)
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Add new product (Admin)


- `GET /api/cart/:sessionId` - Get cart contents
- `POST /api/cart/:sessionId/add` - Add item to cart
- `PUT /api/cart/:sessionId/update` - Update cart item quantity
- `POST /api/cart/:sessionId/promo` - Apply promo code


- `POST /api/orders` - Place order
- `GET /api/orders` - Get orders (all or by session)


- `GET /api/promo-codes` - Get available promo codes
- `GET /api/health` - Health check



- **SAVE10** - 10% discount on total
- **FREESHIP** - Free shipping (₹50 saved)
- **WELCOME20** - 20% discount on total
- **COMBO25** - 25% discount + free shipping

```bash
curl -X POST http://localhost:3000/api/products \
  -H "Content-Type: application/json" \
  -d '{
    "name": "New Product",
    "price": 1999,
    "category": "electronics",
    "description": "Amazing new product",
    "stock": 100
  }'
```


```bash
curl -X POST http://localhost:3000/api/cart/user123/add \
  -H "Content-Type: application/json" \
  -d '{
    "productId": "p1",
    "quantity": 2
  }'
```


Create a `.env` file with:
```env
NODE_ENV=development
PORT=3000
JWT_SECRET=your_secret_key
RATE_LIMIT_MAX_REQUESTS=100
```


The system is designed to easily switch from in-memory storage to MongoDB:
1. Uncomment MongoDB configuration in `.env`
2. Replace in-memory arrays with MongoDB collections
3. Add mongoose models for Products, Orders, and Carts



```bash

npm test


npm run test:api
```



1. **Products Page**: Browse and search products, add to cart
2. **Cart Page**: Manage cart items, apply promo codes, view totals
3. **Checkout Page**: Complete order with customer information
4. **Admin Page**: Add new products to the store


1. Create Heroku app: `heroku create your-app-name`
2. Push code: `git push heroku main`
3. Set environment variables in Heroku dashboard


1. Connect GitHub repository to Vercel
2. Configure environment variables
3. Deploy automatically on push


```bash
# Build production image
docker build -t ecommerce-cart:prod .

# Run production container
docker run -p 3000:3000 -e NODE_ENV=production ecommerce-cart:prod
```



```
ecommerce-cart-system/
├── index.html          # Frontend application
├── styles.css          # Complete styling
├── app.js              # Frontend JavaScript
├── server.js           # Node.js backend
├── package.json        # Dependencies and scripts
├── .env                # Environment variables
├── Dockerfile          # Docker configuration
├── docker-compose.yml  # Multi-container setup
├── start-dev.sh        # Development startup script
├── start-prod.sh       # Production startup script
└── README.md           # This file
```



- **Rate Limiting**: Prevents API abuse
- **Security Headers**: Helmet.js protection
- **Request Logging**: Morgan middleware
- **Error Handling**: Comprehensive error responses
- **Health Checks**: Monitor application status
- **Caching**: Client-side localStorage backup



- CORS configuration for secure cross-origin requests
- Helmet.js for security headers
- Rate limiting to prevent abuse
- Input validation and sanitization
- Error message sanitization


**Name:** Srikaran G  
**Roll No:** 921023104040  
**Department:** Computer Science and Engineering  
**College:** Nadar Saraswathi College of Engineering and Technology  

**Project:** E-Commerce Cart System - Complete Full-Stack Implementation  
**Date:** October 2025  
**Phase:** 4 (Enhanced with Node.js Backend)





1. **Backend API**: Complete RESTful API with Express.js
2. **Session Management**: Server-side cart persistence
3. **Order Processing**: Full order management system
4. **Security**: Production-ready security middleware
5. **Docker Support**: Containerized deployment
6. **API Documentation**: Comprehensive endpoint documentation
7. **Health Monitoring**: Built-in health check endpoints
8. **Error Handling**: Robust error management
9. **Logging**: Request and error logging
10. **Deployment Ready**: Multiple deployment options

This full-stack implementation demonstrates enterprise-level development practices and is ready for production deployment! 🚀

