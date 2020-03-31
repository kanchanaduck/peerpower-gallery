<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header"><strong>Disk Usage</strong></div>
                    <div class="card-body pl-5">
                        <div class="row">
                            <div class="col-sm-3">Total Size:</div>
                            <div class="col-sm-9"></div>
                        </div>
                        <div class="row">
                            <div class="col-sm-3">No of files:</div>
                            <div class="col-sm-9"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card mt-3">
                    <div class="card-header"><strong>File Usage Compositions</strong></div>
                    <div class="card-body">
                        <table class="table">
                            <thead>
                                <tr>
                                    <th>Type</th>
                                    <th>No of files</th>
                                    <th>Size</th>
                                </tr>
                            </thead>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Home')
        }
    }
</script>
