<script setup >
const siteColor = ref(
  {
    background: "#1DC3F1",
    textcolor: "white"
  }
)
const siteSettings = ref(
  {
    logo: {
      dark: "/roq.png",
      light: "/roqs.png"
    },
    favicon: "/logo.png",
    siteTitle: "Yeerlo Personal - Home",
    siteDescription: "Yeerlo Personal  landing page website.",
    footerText: "Elevate Your Experience - Where Every Event Becomes Unforgettable",
    socialLinks: {
      facebook:"#facebook",
      twitter:"#tweet",
      instagram:"#insta",
      youtube:"#youtube",
      tiktok:"#tiktok"

    },
  }

)
const siteHero = ref(
  {
    Header: "Electrify Your Night: An Unforgettable Journey with MC Yeerlo",
    Paragraph: "Join me for a night of electrifying beats and unforgettable moments. Dive into a world where comedy, music and magic meet. Get ready for an experience that will set your heart racing!",
    imgOne: "/images/sidebiew.webp",
    imgTwo: "/images/sidebiew.webp"
  }
)

const siteEvents = ref([
  {
    "id": 1,
    "title": "Start your journey in SEO",
    "link": "#",
    "duration": "24min",
    "image": "https://picsum.photos/800/600",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  },
  {
    "id": 2,
    "title": "Advanced SEO Techniques",
    "link": "#",
    "duration": "30min",
    "image": "https://picsum.photos/800/601",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  },
  {
    "id": 3,
    "title": "SEO for E-commerce",
    "link": "#",
    "duration": "28min",
    "image": "https://picsum.photos/800/602",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  },
  {
    "id": 4,
    "title": "Mastering Local SEO",
    "link": "#",
    "duration": "22min",
    "image": "https://picsum.photos/800/603",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  },
  {
    "id": 5,
    "title": "SEO Analytics and Reporting",
    "link": "#",
    "duration": "35min",
    "image": "https://picsum.photos/800/604",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  },
  {
    "id": 6,
    "title": "Mobile SEO Best Practices",
    "link": "#",
    "duration": "26min",
    "image": "https://picsum.photos/800/605",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  },
  {
    "id": 7,
    "title": "SEO and Content Strategy",
    "link": "#",
    "duration": "40min",
    "image": "https://picsum.photos/800/606",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  },
  {
    "id": 8,
    "title": "International SEO Tactics",
    "link": "#",
    "duration": "32min",
    "image": "https://picsum.photos/800/607",
    "category": "",
    "createdAt": "",
    "description": "Lorem ipsum dolor sit amet, voluptates porro"
  }
]
)
const subscribeText = ref({
  head: "Subscribe  to recieve updates on my upcoming events",
  color: siteColor.value.background,
  text: "By subscribing , you'll get the latest news and updates about all my upcoming events delivered straight to your inbox. Stay connected and be the first to know about exciting new happenings!"
})

useHead({
  title: siteSettings.value.siteTitle,
  meta: [
    { name: 'description', content: siteSettings.value.siteDescription },
  ],
  link: [
    { rel: 'icon', type: 'image/png', href: siteSettings.value.favicon }
  ],
})

</script>
<template>
  <div>
    <AppHeader :siteLogo="siteSettings.logo" :siteColor="siteColor" />
    <SectionsHomeHeroSection :siteHero="siteHero" :siteColor="siteColor" />
    <SectionsHomePopularPodcasts :siteColor="siteColor" :siteEvents="siteEvents" />
    <SectionsCallToAction :subscribeText="subscribeText" />
    <AppFooter :siteSettings="siteSettings" :siteColor="siteColor" />
  </div>
</template>