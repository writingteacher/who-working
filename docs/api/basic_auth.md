---
layout: page
---

# Basic authentification

API requests must provide your username and password in the HTTP Authorization header, encoded in Base64, in your API requests per the Basic Auth specification (see link below).


http://localhost:3000/basic-auth
```

curl -u user:pass http://localhost:3000/workers/2
{
  "last_name": "Jones",
  "first_name": "Jill",
  "email": "j.jones@example.com",
  "phone": "416-555-1212",
  "id": "2",
  "city": "Toronto",
  "available": "mornings",
  "username": "demo",
  "password": "1234"
}

---

**NOTE:**
cURL comes installed by default on Mac operating systems. If you need to, install it from [here](https://curl.se/windows/).

---

## Next steps

Now that you’ve everything set up correctly, you’re good to go and can take full advantage of the Wh's Working service API! Go ahead and start posting new shifts or enrolling new workers. 

If you need more guidance, the Tutorials section of the API documentation walks through any task you’ll want to do. The finer details of the supported resources, endpoints and properties are in the API reference section. For more information, contact the [support team](https://example.com/).
