URL: https://www.youtube.com/watch?v=pAUIaIU7BtQ&list=PLMTCTd3b8IdLkjpCLrxbFKTY6CTlaMPco&index=1

# Disclaimer
There are exceptions to rules. Every rule we've made in networking, we've probably broken it later with a new protocol or a new technology, but these are the foundational guidelines.

# Shared Language
Let's say we have 2 computers and they need a shared language to talk to you and they need a connection between them. So, we connect an electrical wire between A and B computers. We have to agree on a basic unit of communication and since all we got is an electrical wire we'll say +5 volts on the wire means a "1" and -5 volts means "0" for example. We'll use this to encode data onto that wire so we can signal each other.

A **network protocol** at its at its core is just a string of ones and zeros.

one or zero one two three

four five six seven eight nine that's

more complex right that requires a lot

more complexity encoding so when the

folks were just starting and come up

with kind of the fundamentals of how

computers would talk to each other and

in fact computers would write data they

used ones and zeros okay because those

are really easy for both sides to

understand humans obviously like to use

numbers in the decimal number system a

10 base number system binary is just a

to base number system only two options

we'll talk about that more later on them

so we're gonna call each one or zero

option a bit okay that's the name for an

option of a one or zero and if we put

eight of those together we'll call that

a byte

and so in networking we talked about the

unit of data transfer as megabits or

kilobits per second one kbps megabits

per second gigabits per second we even

go up to 10 gigabits 100 gigabit links

so that's how many of these wonders your

options can be transferred in a second

by our network medium whatever that is

so if a real simple network here just

two computers

and when you have two computers on the

network we both know who we're talking

to right there's only one other person

out there so when alice is sending to

Bob just send some data and vice-versa

the only complexity is if that they were

both to talk at the same time they

should they would they would basically

create this electrical voltage that is

neither say a +5 or a -5 they would sum

the voltages together so

in that case we'd have a collision on

that wire and maybe the easiest way to

do it would be we just back off a random

amount of time and then each treat each

try sending that transmission again and

conversely if if we hear the other

person's transmitting me shouldn't

transmit as well okay now what what

complexity is added when we have more

than two devices well we got to know who

we're talking to we can't just assume

when we talk that the other person will

know the transmissions for them so kind

of the obvious idea here is let's assign

each of these computers and address so

Alice will be a Bob Lloyd beasts and he

will be C so whenever we send data we

use their address to communicate so now

we're going to talk about the basics of

a frame we're going to introduce that

concept for the first time and a frame

is just a it's just a piece of data and

what will happen and what will represent

in the time-space is is maybe we'll put

the destination address here and then

the source address here so who's sending

the message and the message contents so

first we'll put the bits for the the be

there we'll put the bits to represent an

a and then the bits to represent a

message context and transmit that on

this shared wire here so here's a little

little example of that Alice sends a

packet there to Bob

so really A to B and that packet or that

frame really and we'll talk about the

distinction later but we'll use them

interchangeably for now

get sent on to this shared electrical

wire and gets forwarded on to Bob and to

Cindy down there so Bob receives the

frame and it says up that's for me the

destination is B and I have the B

address Cindy receives the frame as well

because remember this is just a shared

electrical wire this is a piece of

electrical cable here and so Cindy looks

at the message and said oh that's to be

so I'm in it discard it okay so so here

we have you know the destination the

source and the message we have the

basics of a protocol when we talk about

protocols extensively networking but all

we're really talking about is something

like when you answer the phone

so when somebody picks up the phone they

say hello and the person on the other

end says oh hey Alice it's Bob and then

maybe else will say Oh heya Bob how are

you now a protocol violation would be

something where somebody's rude you know

somebody just answers the phone says hey

what's your problem you know they see

the caller ID and they're upset so

that's a protocol violation but you'll

notice just in human communication and

natural language we have some kind of

protocols for the way we speak and how

things work same with computers so the

the type of network we have set up here

is kind of indicated by the little red

portion of the drawing there is a shared

bus topology okay that means that we

just have one electrical wire that

everybody is on everybody sees everybody

else's electrical transmission when

somebody sends a one or a zero or a

frame a combination of ones or zeroes

everybody sees that and that's kind of a

limitation for us because that means

everybody on this shared electrical wire

can hear everything that's sent to

everybody okay and we have to connect

this shared wire to all basically in a

in a row to all of our different

computers and worse than that if one

computer breaks that'll break that

electrical wire that'll cause us

problems so this is how networking was

done for a lot of years but it's got to

be a better way so a long time ago they

introduced hubs and and hubs allowed us

to change the land of our network a

little bit

so all the computers would connect to

this central location and each of the

computers has a dedicated electrical

wire to that hub okay so if one computer

disconnected from the hub it wouldn't

break that shared electrical connection

the hub would maintain that persistently

for all the different computers so this

network physically from how it's

physically laid out in space is what

we'll call us call a star topology okay

all the computers connect to a central

point but logically how the how the

packets are moving through our network

we still have that shared bus behind the

scenes we still have the architecture

where everybody sees everything all the

time everybody hears every packet of

data that's sent out okay so a physical

versus a logical topology are different

physically they're connected as a star

now rather than a bus but logically we

saw off the bus inside that hub

everybody sees everything so another

problem we have is when when two packets

are sent on to that shared logical glass

inside the hub at the same time again

they create a combination of their

electrical voltages and that's a

collision that's what we call a

collision and then working two packets

collide so the computers will sense

something went wrong in that

transmission and what they'll do is

everybody everybody has to discard that

frame and and back off and try again

okay so one of the one of the things we

use in the ethernet standard and we'll

talk about Ethernet more later is a

protocol called carrier sense multiple

access with collision detection that's

just the formal name for sensing that

somebody else is sending data on the

wire at the same time and detecting

collisions so you'll hear that that

acronym csma/cd

so the collision thing is obviously a

real big problem especially as you add

more and more devices we only have four

right now but man oh man can you imagine

if you had a hundred so to solve the

problem folks invented the switch and

now with the switch eat each port each

port on the switch that a computer

connects to has its own electrical bus

and therefore it has its own collision

domain we call it and the switches are

really smart and this is the cool thing

about switches and we'll talk about a

couple of cool things but switches are

smart and that they won't forward a

packet on to another devices wire if

they know somebody's already

transmitting data so they have the

ability to kind of hold on to packets

and cue them we call it and then forward

them out in order when they're ready

let's talk about another concept then

half duplex flushers this full duplex

communication half duplex means it

simply means you can only send or

receive at the same time one or the

other but not both full duplex

communication or connectivity means that

a device can send data at the same time

it's receiving data can do both so

obviously we prefer full duplex

communication it actually doubles the

available bandwidth so solving the

collision problem so when we were able

to combine switches that can store

packets and then put them in a queue and

forward them out later with full duplex

device

and cabling we can ensure that

collisions don't a cure because there's

a separate send and receive path is

indicated there by the the red and the

blue arrows and the switches holding

that packet and waiting and sending him

in order it's like a a line at a ride or

something like that so other bad things

can happen the packets and that's kind

of beyond the scope of this little talk

right now but but at least the collision

problem is solved and that's really

helpful as we scale out to hundreds or

even thousands of devices more about

switches we talked about switches being

intelligent but not only do they they

solve the collision problem by breaking

up what we call the collision domain but

they intelligently send packets to the

correct port remember when a hub we had

a hub installed that packet that would

come in from a would be heard by B C and

D what a switch can do is it can solve

that problem so packets that are

destined to see from a only get heard by

C B and D aren't even aware of that

that's good from a security perspective

and just from a scalability perspective

so other computers don't have to do as

much work to do this what they do is

they maintain an address table okay and

all that is is the switch when it

receives a packet say on port 1 it said

whose that packet from ok it's from a

computer with the address a well let me

make a table in memory let me say I've

heard computer a on port 1 or if B sends

a packet I've heard computer B on my

port 2 so now if somebody sends a packet

to be a switch we'll know up just just

forward it to port 2 because I know B is

over there for the time being

well what if a switch doesn't know the

address yet maybe it hasn't seen that

device transmitted before we'll all

it'll do then is take the packet and

broadcast it out and also computers

themselves can send broadcast packets

that they need you we'll talk about

broadcast packets later on in the series

but all we're saying there is we don't

know who the packet is is going to be

sent to or the switch doesn't know where

that that destination is so in that case

it just floods the packets out to all of

its ports - the port that it received

the traffic from okay so when a

broadcast is sent out the basically the

radius that the the grouping of devices

that will hear that broadcast packet is

called a broadcast domain so we had the

collision domain earlier who is

everybody that'll tear the collision and

then we have a broadcast domain what is

the the group of computers that will

receive any given broadcast so as our

networks grow and we add more and more

devices like we said into the hundreds

maybe your thousands even the amount of

traffic related to broadcast frames is

significant because each packet when it

gets broadcasted out has to go to each

computer so we need a way to break up

broadcast domains how far that

broadcasts go and and so to do this
we'll insert a piece of gear called a
router basically we need to route
traffic between segments so this is
where a router comes in okay routers
segment networks into separate broadcast
domains they do this this way they don't
Ford broadcast packets that they receive
onto other networks so here on the left
if a broadcast packet were sent out
get rid of the menu bar here so on the
left if a broadcast packet were sent
over here
it wouldn't be heard over here on this
side of the router so it divides that
broadcast domain in half the other nice
thing that routers do and we'll talk
about this a lot more later is they can
some summarize the addresses used on
each segment of the network so over here
on this this left side they say this
group of addresses over here maybe ABC
and over on the right side de F are used
okay so in practice networks are
combined are comprised of a lot of
routers in fact the internet one of that
kind of course theses here is the
Internet is a giant network of routers
and the routers job is to find the best
path to get closer to the destination in
that packet remember we talked about a
packet from A to B well the router may
not know exactly how to get to B but at
least it'll get closer and we'll do this
by forwarding the packet from hop to hop through the network hopefully in the best path you can see there's some inefficient paths here so we could go from this red guy over to the white over the white back to the red that would be kind of inefficient it would seem but the router will trying to find the best path through the network to the destination maybe B's over here okay well that's it for our first segment and the next segment will go way deeper into how packets are constructed and the ins and outs of network subnets and addresses alright thanks