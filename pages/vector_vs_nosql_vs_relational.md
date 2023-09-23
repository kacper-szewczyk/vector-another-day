
# Relational Databases

<div style="margin-top: 16px" v-click="1">

### Insert
Complexity O(1) <spam style="font-weight: bold">+ time to generate indexes</spam>

</div>

<div style="margin-top: 16px" v-click="2">

### Search
Complexity O(n) / O(log(n)) with index, but it's exact match

</div>
<div style="margin-top: 16px" v-click="3">


### Removing
Complexity O(n) / O(log(n)) with index
</div>

::right::

# Vector Databases

<div style="margin-top: 16px" v-click="1">

### Insert
Complexity O(1)

</div>

<div style="margin-top: 16px" v-click="2">

### Search
Complexity O(log(n)), returns approximate match
</div>

<div style="margin-top: 16px" v-click="3">

### Removing
Complexity O(log(n))
</div>