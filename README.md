## Go Kafka demo
### Inspired by Akhil Sharma (https://github.com/AkhilSharma90/GO-Kafka-Example/tree/master)

## Running the project
- first run `docker-compose up -d`
- run `go run producer/producer.go` and `go run consumer/consumer.go`

## Test it 
Send POST request to `http://localhost:6000/comments` with headers `'Content-Type: application/json'`.
Body:
`
{
  "text":"hello, world!"
}
`

Response:
`
{
    "comment": {
        "text": "hello, world!"
    },
    "message": "Comment pushed to queue successfully",
    "success": true
}
`

Consumer log:
`
Received message count: 1 | Topic: comments | Message ({"text":"hello, world!"})
`