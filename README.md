
```

sudo systemctl stop portfolio 2>/dev/null || true

git clone https://github.com/webwizarding/improved-octo-barnacle.git

mv improved-octo-barnacle portfolio

npm install

cd /home/portfolio
DB="file:/home/portfolio/data.sqlite" NEXT_SKIP_BUILD_STATIC_GENERATION=1 npm ci
DB="file:/home/portfolio/data.sqlite" NEXT_SKIP_BUILD_STATIC_GENERATION=1 npm run build

sudo systemctl enable --now portfolio
sudo systemctl status portfolio --no-pager -n 10
```
