<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header"><strong>Gallery</strong></div>
                    <div class="card-body">
                        <vue-dropzone class="mb-3" ref="myVueDropzone" id="dropzone" :options="dropzoneOptions" :useCustomSlot=true>
                            <div class="dropzone-custom-content">
                                <h1 class="dropzone-custom-title display-3"><i class="fas fa-cloud-upload-alt"></i></h1>
                                <div class="subtitle">Drop files here or click to choose files..</div>
                            </div>
                        </vue-dropzone>
                        <div class="row">
                            <div class="col-4" v-for="img in imgs" :key="img.id">
                                <div class="img-container">
                                    <img v-bind:src="'image/'+ img.src ">
                                    <ul class="img-manage">
                                        <li><a class="btn btn-info"><i class="fas fa-search"></i></a></li>
                                        <li><a class="btn btn-danger"><i class="far fa-trash-alt"></i></a></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import vue2Dropzone from 'vue2-dropzone'
import 'vue2-dropzone/dist/vue2Dropzone.min.css'
export default {
    name: 'app',
    components: {
        vueDropzone: vue2Dropzone
    },
    data: function () {
        return {
            dropzoneOptions: {
                url: 'https://httpbin.org/post',
                thumbnailWidth: 150,
                maxFilesize: 0.5,
                headers: { "My-Awesome-Header": "header value" },
            },
            imgs: [
                { 
                    id: 1,
                    src: 'aquarium.png' 
                },
                {   
                    id: 2,
                    src: 'aquarium.png' 
                },
                {   
                    id: 3,
                    src: 'aquarium.png' 
                }
            ]
        }
    }
}
</script>

<style scoped>
#dropzone{
    border: dashed;
}
.img-container img {
  width: 100%;
  height: auto;
}
.img-container .img-manage {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  list-style: none;
}
.img-container .img-manage a {
    color: #fff;
}
</style>
