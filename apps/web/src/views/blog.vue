<template>
    <h1 class="w-full h-fit" v-if="!props.download">&lt;Blog /&gt;</h1>
    <BlogTile :download="props.download" title="Cybersec Europe" date="30/05/2024">
        <BlogCybersec />
    </BlogTile>
    <BlogTile :download="props.download" title="Veeam talk by Nico Losschaert" date="29/04/2024">
        <BlogVeeam />
    </BlogTile>
    <BlogTile :download="props.download" title="Jobhappening Kortrijk" date="21/03/2024">
        <BlogJobHappening />
    </BlogTile>
    <BlogTile :download="props.download" title="Cyber Security Challenge 2024" date="08/03/2024 - 09/03/2024">
        <BlogCyberSecChalenge2024 />
    </BlogTile>
    <BlogTile :download="props.download" title="Embrace the Future of the Internet with Belgian IPv6 Council Meetups" date="21/11/2023">
        <BlogGoogleIP />
    </BlogTile>
    <BlogTile :download="props.download" title="Dcstar Hosting Company Visit">
        <BlogHostingCompanyVisit />
    </BlogTile>
    <BlogTile :download="props.download" title="Conxion">
        <BlogConxion />
    </BlogTile>
    <BlogTile :download="props.download" title="Secutec Security Summit" date="16/11/2023">
        <BlogSecutecSecuritySummit />
    </BlogTile>
    <BlogTile :download="props.download" title="Hacking Garage Doors With RF" date="25/10/2023">
        <BlogHackingGarageDoorsWithRF />
    </BlogTile>
    <BlogTile :download="props.download" title="Campus Cloud Cafe" date="17/10/2023">
        <BlogCloudCafe />
    </BlogTile>
    <BlogTile :download="props.download" title="Digitilize Flanders" date="04/10/2023">
        <BlogDigitilizeFlanders />
    </BlogTile>
    <BlogTile :download="props.download" title="Stagemarkt">
        <BlogStagemarkt />
    </BlogTile>
    <BlogTile :download="props.download" title="International Project Week" date="03/07/2023-07/07/2023">
        <BlogInternationaleProjectWeek />
    </BlogTile>
    <BlogTile :download="props.download" title="Cyber Security Challenge 2023">
        <BlogCyberSecChalenge2023 />
    </BlogTile>
    <BlogTile :download="props.download" title="Welcome to my blog!">
        <BlogFirstPost />
    </BlogTile>
</template>

<script setup lang="ts">
    import BlogConxion from '@/components/Layout/Pages/blog/BlogConxion.vue';
    import BlogHostingCompanyVisit from '@/components/Layout/Pages/blog/BlogHostingCompanyVisit.vue';

    interface IProps {
        download?: boolean;
    }

    const props = withDefaults(defineProps<IProps>(), {});

</script>

<style scoped></style>
