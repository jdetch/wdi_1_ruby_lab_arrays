require 'pry'

tweet = "We ate fifty cheeseburgers for lunch"
tweet_words = tweet.split

binding.pry

long_words = tweet_words.select{ |tweet| tweet.length > 3}

# also can do
# long_words = tweet_words. select do |word|
#   word.length > 3
# end

binding.pry

hashtags = long_words.map do |word|
  '#' + word
# could also do: '##{word}'
end

tagged_tweet = tweet + ' ' + hashtags.join(' ')

