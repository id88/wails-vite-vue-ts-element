<template>
    <h2>{{ msg }}</h2>
    <div class="card">
        <button type="button" @click="count++">count is {{ count }}</button>
    </div>
    <el-row class="mb-4">
        <el-button>Default</el-button>
        <el-button type="primary">Primary</el-button>
        <el-button type="success">Success</el-button>
        <el-button type="info">Info</el-button>
        <el-button type="warning">Warning</el-button>
        <el-button type="danger">Danger</el-button>
    </el-row>
    <br>
    <el-row class="mb-4">
        <el-button plain>Plain</el-button>
        <el-button type="primary" plain>Primary</el-button>
        <el-button type="success" plain>Success</el-button>
        <el-button type="info" plain>Info</el-button>
        <el-button type="warning" plain>Warning</el-button>
        <el-button type="danger" plain>Danger</el-button>
    </el-row>
    <br>
    <el-row class="mb-4">
        <el-button round>Round</el-button>
        <el-button type="primary" round>Primary</el-button>
        <el-button type="success" round>Success</el-button>
        <el-button type="info" round>Info</el-button>
        <el-button type="warning" round>Warning</el-button>
        <el-button type="danger" round>Danger</el-button>
    </el-row>
    <br>
    <el-row>
        <el-button :icon="Search" circle />
        <el-button type="primary" :icon="Edit" circle />
        <el-button type="success" :icon="Check" circle />
        <el-button type="info" :icon="Message" circle />
        <el-button type="warning" :icon="Star" circle />
        <el-button type="danger" :icon="Delete" circle />
    </el-row>
    <br>
    <div class="flex">
        <el-button type="primary" :icon="Edit" />
        <el-button type="primary" :icon="Share" />
        <el-button type="primary" :icon="Delete" />
        <el-button type="primary" :icon="Search">搜索</el-button>
        <el-button type="primary">
            上传<el-icon class="el-icon--right"> <Upload /> </el-icon>
        </el-button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

import {
    Check,
    Delete,
    Edit,
    Message,
    Search,
    Star,
    Share,
    Upload 
} from '@element-plus/icons-vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<style scoped>
</style>
