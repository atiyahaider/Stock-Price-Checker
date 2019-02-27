**FreeCodeCamp**- Information Security and Quality Assurance
------

Stock Price Checker

**User Stories**

1. Set the content security policies to only allow loading of scripts and css from the server.
2. **GET** /api/stock-prices with form data containing a Nasdaq stock ticker and recieve back an object stockData.
3. stockData contains the stock(string, the ticker), price(decimal in string format), and likes(int).
4. My like can be added to the stock(s), by passing along field `like` as true(boolean). Only 1 like per IP would be accepted.
5. If 2 stocks are passed along, the return object will be an array with both stock's info, but instead of likes, it will display rel_likes(the difference between the likes on both) on both.
6. A good way to receive current price is the following external API(replacing 'GOOG' with your stock): https://api.iextrading.com/1.0/stock/goog/price
7. All 5 functional tests are complete and passing.

**Example usage:**

`/api/stock-prices?stock=goog
/api/stock-prices?stock=goog&like=true
/api/stock-prices?stock=goog&stock=msft
/api/stock-prices?stock=goog&stock=msft&like=true`

**Example return:**

`{"stockData":{"stock":"GOOG","price":"786.90","likes":1}}`

`{"stockData":{"stock":"MSFT","price":"62.30","rel_likes":-1},"stock":"GOOG","price":"786.90","rel_likes":1}]}`

[Front End](https://holy-basketball.glitch.me/)