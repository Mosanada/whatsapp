# Download the helper library from https://www.twilio.com/docs/python/install
from twilio.rest import Client


# Your Account Sid and Auth Token from twilio.com/console
# DANGER! This is insecure. See http://twil.io/secure
account_sid = 'AC04a6d18678b36520bfe8b51a88361d47'
auth_token = 'ed008d2698758c7e1762ae2f48825c91'
client = Client(account_sid, auth_token)

message = client.messages.create(
                              from_='+18773659741',
                              body='body',
                              to='+15558675310'
                          )

print(message.sid)
