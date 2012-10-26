### Is the author of rspec mock living in the same area as me?

From [rspec mock rdoc page](http://rubydoc.info/gems/rspec-mocks/frames)

## Message Expectations
A message expectation is an expectation that the test double will receive a message some time before the example ends. If the message is received, the expectation is satisfied. If not, the example fails.

validator = double("validator")
validator.should_receive(:validate).with("02134")
zipcode = Zipcode.new("02134", validator)
zipcode.valid?