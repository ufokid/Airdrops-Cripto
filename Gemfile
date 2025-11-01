source 'https://rubygems.org'
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

ruby '3.2.0'

# Core Rails
gem 'rails', '~> 7.0.0'
gem 'puma', '~> 5.0'

# Database
gem 'pg', '~> 1.1'

# Frontend
gem 'webpacker', '~> 5.0'
gem 'react-rails'
gem 'sass-rails', '>= 6'
gem 'bootstrap'

# API & Data
gem 'jbuilder', '~> 2.7'
gem 'httparty'
gem 'faraday'
gem 'json', '~> 2.5'

# Authentication
gem 'devise'
gem 'jwt'
gem 'pundit'

# Database utilities
gem 'redis', '~> 4.0'
gem 'sidekiq'

# Crypto/Blockchain
gem 'eth'
gem 'web3-eth'
gem 'bitcoin-ruby'

# Environment
gem 'dotenv-rails'
gem 'aws-sdk-s3'

# Monitoring & Logging
gem 'sentry-ruby'
gem 'sentry-rails'

# Testing
group :development, :test do
  gem 'byebug', platforms: [:mri, :mingw, :x64_mingw]
  gem 'rspec-rails'
  gem 'factory_bot_rails'
end

group :development do
  gem 'web-console', '>= 4.1.0'
  gem 'listen', '~> 3.3'
  gem 'spring'
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]
