## Muuuuuuuuh...oose?!
#### An introduction to Moose - the Extension of the Perl Object System

---

### Postmodern and tre chic
### - the agenda

---

* OOP before and after Moose
* What is Moose?
* Let's go deeper!
* "May I ask a question?" - so meta
* Conclusion

---

### Alexander Kluth
#### Lead Developer & SRE
### Nexus Netsoft Group

* 26 years old
* Married to the most wonderful girl in the world
* 95% PHP, 5% Perl @ Work
* Co maintainer CGI.pm
* YAPH, Rust enthusiast, "young C veteran"

---

## Perl and OOP - back then

---

There were times...

People used to write code like
  
...this:

---

```
package Rocket;

sub new {
    my ($class, %param) = @_;
    my $object = bless ({'v' => $param{speed} }, $class);
    return $object;
}

sub stop {
    my ($object) = shift;
    $object->{'v'} = 0;
}
```

---

Today it's more like...

---

```
package UFO;
use Moose;

has 'speed' => (is => 'rw');

sub stop {
    my ($object) = shift;
    $object->speed(0);
}
```
