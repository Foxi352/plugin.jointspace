# Jointspace

# Supported Hardware

Tested with:
* Philips 37PFL9604H/12

Should work with all Philips TV sets > 2010 (http://jointspace.sourceforge.net)

# Configuration

## plugin.conf

<pre>
[jointspace]
    class_name = Jointspace
    class_path = plugins.jointspace
    host = &lt;ip&gt;
#   port = &lt;port&gt;
</pre>

Description of the attributes:

* __host__: IP or hostname of the TV set
* __port__: Port number of Jointspace running on the TV set, normally telnet port 1925

## items.conf example

<pre>
[TV]
	type = bool
	visu_acl = rw
	jointspace_cmd = power
	enforce_updates = on
	[[Mute]]
		type = bool
		visu_acl = rw
		jointspace_cmd = mute
		enforce_updates = on
	[[Volume]]
		type = num
		visu_acl = rw
		jointspace_cmd = volume
		enforce_updates = on		

</pre>

## pages example

<pre>
</pre>