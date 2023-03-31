# Steps to make a lambda layer

The following steps can be used to create a lambda layer. In this example we create one with the kafka-python package.


```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
mkdir -p kafka-layer/python
cp -r venv/lib kafka-layer/python/
cd kafka-layer
zip -r kafka-layer.zip .
unzip -l kafka-layer.zip
```

Now upload kafka-layer.zip to the AWS console (Lambda Layers) and note the version ARN

Use this version ARN in your Lambda function