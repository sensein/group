# The Group Website

This is the website of our academic research group at MIT.

This website is powered by Jekyll and some Bootstrap, Bootwatch. Go to 
*aboutwebsite.md*  to learn how to copy and modify this page for your purpose. 


A big thank you to https://github.com/mpa139/allanlab for setting up this 
framework.

### For local development:

```
docker run --rm -it --volume="$PWD:/srv/jekyll" \
  --volume="$PWD/vendor/bundle:/usr/local/bundle"  \
  --env JEKYLL_ENV=development -p 4000:4000 \
  jekyll/jekyll:4.0.1  jekyll serve --config _config.yml
```