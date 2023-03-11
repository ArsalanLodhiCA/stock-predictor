# stock-predictor
stock predictor

curl \
--header "Content-Type: application/json" \
--request POST \
--data '{"ticker":"MSFT", "days":7}' \
http://35.93.74.139:8000/predict
