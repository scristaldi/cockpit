<!--
Copyright (C) 2022 Josh Boudreau <jboudreau@45drives.com>

This file is part of Cockpit File Sharing.

Cockpit File Sharing is free software: you can redistribute it and/or modify it under the terms
of the GNU General Public License as published by the Free Software Foundation, either version 3
of the License, or (at your option) any later version.

Cockpit File Sharing is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY;
without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with Cockpit File Sharing.
If not, see <https://www.gnu.org/licenses/>. 
-->

<template>
	<div class="flex flex-row flex-wrap space-x-2">
		<PillListItem v-for="(item, index) in list" :item="item" @remove-item="$emit('remove-item', item)"/>
	</div>
</template>

<script>
import PillListItem from "./PillListItem.vue";
export default {
    props: {
        list: Array
    },
    components: { PillListItem },
}
</script>

<style scoped>
</style>
