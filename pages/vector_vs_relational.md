
# Relational Database

<div v-click="1" style="margin-top: 16px">

### Add new element
Time complexity O(1) <spam style="font-weight: bold" v-click="7">+ time to generate index</spam>

</div>

<div v-click="3" style="margin-top: 16px">

### Search element
Time complexity O(n) or O(log n) with index, but match is exact

</div>
<div v-click="5" style="margin-top: 16px">

### Delete element
Time complexity O(n) or O(log n) with index  
</div>

::right::

# Vector Database

<div v-click="2" style="margin-top: 16px">

### Add new element
Time complexity O(1)

</div>

<div v-click="4" style="margin-top: 16px">

### Search element
Time complexity O(log n), returning approximate match
</div>

<div v-click="6" style="margin-top: 16px">

### Delete element
Time complexity O(log n)
</div>