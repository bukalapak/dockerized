# dockerized

To create a new image, please use this command:

```bash
set -e

TAG=${1:-bukalapak/<identifier>} #please change <identifier> with project you're working for example ruby-2.3

exec docker build -t "$TAG" .
```