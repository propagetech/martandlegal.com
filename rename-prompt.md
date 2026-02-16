You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Martand Legal Advisors | About Us",
      "first_heading": "About Us"
    }
  },
  {
    "path": "appointments-booking.html",
    "context": {
      "title": "Martand Legal Advisors | Appointments / Booking",
      "first_heading": "Appointments / Booking"
    }
  },
  {
    "path": "blog.html",
    "context": {
      "title": "Martand Legal Advisor | News & Deals Closings",
      "first_heading": "News and Deals"
    }
  },
  {
    "path": "blog_nri-investments-in-india.html",
    "context": {
      "title": "NRI Investments in India",
      "first_heading": "NRI Investments in India"
    }
  },
  {
    "path": "blog_trust-vs--society.html",
    "context": {
      "title": "Trust vs. Society",
      "first_heading": "Trust vs. Society"
    }
  },
  {
    "path": "career.html",
    "context": {
      "title": "Martand Legal Advisors | Careers",
      "first_heading": "Careers"
    }
  },
  {
    "path": "careers-form.html",
    "context": {
      "title": "Martand Legal Advisors | Apply Form",
      "first_heading": "Apply Form"
    }
  },
  {
    "path": "contact.html",
    "context": {
      "title": "Martand Legal Advisors | Contact Us",
      "first_heading": "Contact Us"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/47199a09e42d8056913f4a8ecfae0607.css",
    "context": {
      "path": "css/47199a09e42d8056913f4a8ecfae0607.css"
    }
  },
  {
    "path": "css/499b3ed2a6ddcf3ffddcfb451ff19aee.css",
    "context": {
      "path": "css/499b3ed2a6ddcf3ffddcfb451ff19aee.css"
    }
  },
  {
    "path": "css/4e29500e460a782764d934bd2d80696f.css",
    "context": {
      "path": "css/4e29500e460a782764d934bd2d80696f.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/023461cf6e7eca94b7f97df23467ee9b.webp",
    "context": {
      "refs": [
        {
          "alt": "Patents",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/037d8b860e6d3fa5cb7b666307643825.webp",
    "context": {
      "refs": [
        {
          "alt": "Lawyers, Charted Accountants and Registered Authorizers.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/08e30ce95340d95cbf817d703e1bba7c.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1f9140114860483b6f47204bef42c1a6.webp",
    "context": {
      "refs": [
        {
          "alt": "Designs",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b9060eebc52561d616f9497da26cf12.webp",
    "context": {
      "refs": [
        {
          "alt": "M&A",
          "title": ""
        },
        {
          "alt": "M&A",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/473f8e344db7526f29daecb510514bdf.webp",
    "context": {
      "refs": [
        {
          "alt": "MISSION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/49fdfac6b302b3da7743eb5740be7120.webp",
    "context": {
      "refs": [
        {
          "alt": "FEMA",
          "title": ""
        },
        {
          "alt": "FEMA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4fa43d211c29bf7757441ea69894cc97.webp",
    "context": {
      "refs": [
        {
          "alt": "ESOP Management Tool",
          "title": ""
        },
        {
          "alt": "ESOP Management Tool",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/515e46f77e5cf2ecc422b8dc2dcc5f78.webp",
    "context": {
      "refs": [
        {
          "alt": "VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55377f2fc83236e9f14ebfd16492ec28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/59994dc66aa61869a0d4187c2d542171.webp",
    "context": {
      "refs": [
        {
          "alt": "Your partner for legal services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e97a5fd8b5f28cc421777bb23939309.webp",
    "context": {
      "refs": [
        {
          "alt": "Setting up Office in India",
          "title": ""
        },
        {
          "alt": "Setting up Office in India",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6dcfdd38fcddf18d57fb4f26590cbcc4.webp",
    "context": {
      "refs": [
        {
          "alt": "Trademark",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8caf217ca1f3a27d6cdd52892c4aa744.webp",
    "context": {
      "refs": [
        {
          "alt": "Copyright",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b183bb784281b2996c925e3fcfcc4de.webp",
    "context": {
      "refs": [
        {
          "alt": "Corporate Agreements",
          "title": ""
        },
        {
          "alt": "Commercial Agreements",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5f58e6f4ec2fb82af597357412a7f5d.webp",
    "context": {
      "refs": [
        {
          "alt": "IP Laws",
          "title": ""
        },
        {
          "alt": "IP Law",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c56f534a59cf802a98a67a18bbdf48ff.webp",
    "context": {
      "refs": [
        {
          "alt": "Corporate Laws & Advisory",
          "title": ""
        },
        {
          "alt": "Corporate Laws & Advisory",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3ce4d958da99d917477c82fa2e700be.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3d4268d115eb3cfce991e02b8fbd068.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1a21bbdaad07709be20fb841218e1be.webp",
    "context": {
      "refs": [
        {
          "alt": "Due-Diligence",
          "title": ""
        },
        {
          "alt": "Due-diligence",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4db0a67adba8333a700e4da27ed47d1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebeced3691593f3c842764a144f8b139.webp",
    "context": {
      "refs": [
        {
          "alt": "Martand Legal Advisor LLP",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6a5f1f67930f9aa177e3bc6bc28330a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Martand Legal Advisors | We strive to provide you legal advisory and compliances services for your Business",
      "first_heading": "Martand Legal Advisors"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/701075b009d10c8dd7b6a175750874db.js",
    "context": {
      "path": "js/701075b009d10c8dd7b6a175750874db.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "news.html",
    "context": {
      "title": "",
      "first_heading": "MCA Notifications on Companies Act, 2013!"
    }
  },
  {
    "path": "practicearea.html",
    "context": {
      "title": "Martand legal Advisors | Our Practice Areas",
      "first_heading": "Our Practice Areas"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.