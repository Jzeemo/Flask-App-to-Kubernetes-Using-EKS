# Flask-App-to-Kubernetes-Using-EKS

# Deploying A Flask API

This project is to deploy a flask app to aws eks cluster and create a CICD pipeline.

## URL

This is the base url to call the app

```bash
a31b0027797c444e28b98d5b5fce0994-1793884570.ap-southeast-1.elb.amazonaws.com
```

#### GET /

* General: Returns a string called "Healthy".
* Sample: `http://a31b0027797c444e28b98d5b5fce0994-1793884570.ap-southeast-1.elb.amazonaws.com`<br>

        "Healthy"




#### POST /auth

* General:
  * Returns a JWT Token.
* Sample: POST Method`http://a31b0027797c444e28b98d5b5fce0994-1793884570.ap-southeast-1.elb.amazonaws.com/auth'
<br>
Body
<br>

```bash
        {
            "email": "usertesting@testing.com",
            "password": "123"
        }
```
Return

       ""token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2MzIxNTUzNTksIm5iZiI6MTYzMDk0NTc1OSwiZW1haWwiOiJ1c2VydGVzdGluZ0B0ZXN0aW5nLmNvbSJ9.4UUKE2k6yg8sPNdo-yPX9dp1C0YXFJiRzT9987clXOo""

#### GET /contents

* General: Returns the token information.
* Sample: `http://a31b0027797c444e28b98d5b5fce0994-1793884570.ap-southeast-1.elb.amazonaws.com/contents`<br>
Header
<br>

        "Header: Authorization Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2MzIxNTUzNTksIm5iZiI6MTYzMDk0NTc1OSwiZW1haWwiOiJ1c2VydGVzdGluZ0B0ZXN0aW5nLmNvbSJ9.4UUKE2k6yg8sPNdo-yPX9dp1C0YXFJiRzT9987clXOo"

Return

```bash
{
    "email": "usertesting@testing.com",
    "exp": 1632155359,
    "nbf": 1630945759
}
```
