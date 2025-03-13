<template>
  <div
    class="max-w-xs bg-white rounded-lg shadow-md overflow-hidden font-sans mx-auto my-5 bg-gradient-to-tr from-gray-300 to-gray-500"
  >
    <div class="text-center p-1">
      <img
        :src="profileImage"
        alt="Profile Image"
        class="w-32 h-32 m-5 rounded-full object-cover border-4 border-gray-200 mx-auto"
        style="object-fit: contain"
      />
      <h1 class="mt-2 mb-1 text-xl font-bold">{{ userName }}</h1>
      <p class="text-gray-600 mb-5">{{ userBio }}</p>
      <div class="text-gray-600 mb-5">
        <a
          v-for="(link, index) in links"
          :key="index"
          :href="link.url"
          target="_blank"
          class="inline-block mx-2"
        >
          <img
            :src="link.img"
            :alt="link.title"
            class="w-8 h-8"
            style="object-fit: contain"
          />
        </a>
      </div>
    </div>
    <div class="p-5">
      <h3 class="mt-2 mb-1 text-xl text-center font-bold">Proyectos</h3>
      <ul>
        <li v-for="(linkBtn, index) in linksBtn" :key="index" class="my-2">
          <a
            :href="linkBtn.url"
            target="_blank"
            class="block text-center py-2 bg-blue-500 text-white rounded transition duration-300 hover:bg-blue-600"
          >
            <span class="text-lg">{{ linkBtn.title }}</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    profileImage: {
      type: String,
      default: "https://img.freepik.com/vector-gratis/ilustracion-dibujos-animados-lindo-bulldog-funcionamiento-portatil-concepto-icono-tecnologia-animal_138676-1912.jpg",
    },
    userName: {
      type: String,
      default: "AUGUSTO SALAZAR",
    },
    userBio: {
      type: String,
      default:
        " Soy una persona proactiva, con gran capacidad de aprendizaje, adaptación y trabajo en equipo, siempre dispuesta a contribuir y aprender.",
    },
    links: {
      type: Array,
      default: () => [
        {
          title: "GitHub",
          url: "https://github.com/AugustoSalazar99?tab=repositories",
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/GitHub_Invertocat_Logo.svg/1200px-GitHub_Invertocat_Logo.svg.png",
        },
        {
          title: "WhatsApp",
          url: "https://wa.me/+593993080598",
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/WhatsApp.svg/479px-WhatsApp.svg.png",
        },
        {
          title: "LinkedIn",
          url: "https://www.linkedin.com/in/augusto-salazar-a38078264/",
          img: "https://store-images.s-microsoft.com/image/apps.1719.9007199266245564.44dc7699-748d-4c34-ba5e-d04eb48f7960.abf46174-2d32-4f53-a6cd-644d5b2be452",
        },
        {
          title: "Certificados",
          url: "https://drive.google.com/drive/folders/11YlX4hBxffLW4rmLtqNBrKNfwmF_69a-?usp=sharing",
          img: "https://png.pngtree.com/png-clipart/20230817/original/pngtree-certificate-icon-design-outline-color-style-degree-certificate-achievement-vector-picture-image_10948913.png",
        },
      ],
    },
    linksBtn: {
      type: Array,
      default: () => [
        {
          title: "BootStrap con Vue",
          url: "https://bootstrap-vue-six.vercel.app/",
        },
        {
          title: "Tailwind con React",
          url: "https://tailwind-react-murex.vercel.app/",
        },
      ],
    },
  },
};
</script>

<style scoped>
/* No se necesita CSS personalizado, todo está en Tailwind */
</style>
