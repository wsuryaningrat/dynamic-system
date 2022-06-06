# GUI for Dynamic System
Simulations on dynamic models are needed to deepen understanding of population dynamics, the effect of parameter changes, or controls. Especially for complex models that are difficult to approach with analytical methods.

For easy tuning of the developed scheme, a graphical user interface (GUI) is developed under Maple environment.


## User guide:

1. You must first install maple, to run this GUI
2. 

```bash
$ LPUSH macul:default:task '{"event": "SIGN_UP", "body": "{\"email\": "\john.doe@gmail.com"\, \"password\": \"test123$\"}"}'
```

Also the message is must have these two keys `event` with string value and `body` is JSON serializable or any primitive data type.

__Consumer:__
```maple
from macul import Macul


app = Macul()


@app.consumer(event_name='testing')
async def worker_testing(message):
    print('Consumed by: testing')
    print(message)


@app.consumer(event_name='notification')
async def worker_notification(message):
    print('Consumed by: notification')
    print(message)


if __name__ == '__main__':
    app.start()
``` 
