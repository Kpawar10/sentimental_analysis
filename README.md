from smartapi import SmartConnect,SmartWebSocket
import 
import andas as pd
import pyotp
obj = SmartConnect(api_key = "pBv4E6Cn")
data = obj.generateSession("R51358724","2009",pyotp.TOTP("NUQ7FUCLXO662UYUXCWJGIZ6QQ").now())
refreshToken = data['data']['refreshToken']
feedToken = obj.getfeedToken()
print(feedToken)