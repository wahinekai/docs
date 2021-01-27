FROM jekyll/jekyll

WORKDIR /app

COPY . .

# Get around Gemfile.lock errors
RUN touch Gemfile.lock
RUN chmod a+w Gemfile.lock

RUN bundle install

EXPOSE 4000
ENTRYPOINT [ "bundle", "exec", "jekyll", "serve", "--host", "0.0.0.0" ]