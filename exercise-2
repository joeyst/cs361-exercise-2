# Name Mangler
NAME = "Johanna Jackson"

def reverse_words(words)
  words.split.reverse.join(' ')
end

def borgify(string)
  string + " Borg"
end

def words_pipeline(words, *pipe)
  words = words.dup
  pipe.each do |p| words = method(p).call(words) end
  words
end

# Mangle the name by reversing it or borgifying it
def modified_name(choose)
  if choose
    words_pipeline(NAME, :reverse_words, :borgify)
  else 
    words_pipeline(NAME, :reverse_words)
  end
end

puts "New name: #{modified_name(false)}"
puts "New borg name: #{modified_name(true)}"

puts words_pipeline(NAME, :borgify, :reverse_words)