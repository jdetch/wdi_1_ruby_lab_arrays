days = %w(Monday Tuesday Wednesday Thursday Friday Saturday Sunday)

days.insert('Sunday').pop
# Correct = days.unshift(days.pop)
# or days.insert(0, days.pop)
# of days.rotate! > this rotates the wrong way
# days.rotate!(-1) would work

days[days.index('Thursday')].upcase!

nested_days = [%w(Monday, Tuesday, Wednesday, Thursday, Friday), %w(Saturday Sunday)]

# 0 calls first array of the 2 arrays and 2 refers to element 2
# of that array ('Wednesday')
nested_days[0][2] = "Woden's Day"

nested_days.shift

sorted_days = days.sort

sorted_days.each do |day|
  puts day
end
