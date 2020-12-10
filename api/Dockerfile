FROM ruby:2.5.7
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
WORKDIR /api
COPY Gemfile /api/Gemfile
COPY Gemfile.lock /api/Gemfile.lock
RUN gem update --system \
    && gem install bundler -v 2.1.0 \
    && bundle install
COPY . /api

# Start the main process.
CMD ["rails", "server", "-b", "0.0.0.0"]