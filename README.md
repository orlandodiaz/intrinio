### Description
Save ticker symbols from Intrinio's stock screening API.
### Usage

Fill in credentials:

    email = 'your.email@gmail.com'
    password = 'your.pass' 
    intrinio = Intrinio(username, password)

Intrinio's screener API settings can be found at http://blog.intrinio.com/stock-screener-api-intrinio/

    # Market-cap greater than 2 billion
    intrinio.url = 'https://api.intrinio.com/securities/search?conditions=marketcap~gt~2000000000&page_size=500'
    
Start request

    symbols = intrinio.get_stocks()
    
Save for later

    intrinio.save(symbols, "less_than_200m.p")  