# Grow Your Unix Beard Using Ruby

An overview of Unicorn internals

### Slides

Soon...

### Notes

- Forking with Ruby
- Forking creates an exact copy and they don't share memory
- Pre-forking with ruby

#### Unicorn

- All processes spawn in Unicorn do fork+exec because exec exists the process after finishing
- JRuby doesn't implement fork to be cross-platform

### Books

[http://workingwithcode.com/](http://workingwithcode.com/)