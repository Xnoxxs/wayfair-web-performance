# **Stakeholders Audit** 

Wayfair delivers a visually polished shopping experience with strong accessibility, SEO, and a modern front-end architecture. However, the website suffers from significant client-side performance issues caused primarily by large JavaScript bundles and numerous third-party integrations. 

These issues increase page load time, delay user interaction, and create a slower shopping experience, particularly for first-time visitors and users on slower devices. Poor performance can negatively affect customer engagement, conversion rates, and search visibility. 

Not all improvements require major architectural changes. Several high-impact optimizations can be implemented with relatively low development effort, while a smaller number of structural improvements require longer-term investment. 

# **Overall Assessment** 

**Area Assessment** 

Business Risk Medium–High User Experience Moderate SEO Impact Moderate Conversion Impact High 

Estimated Implementation Effort Low–High (depends on recommendation) 

# **What Is Working Well** 

### **Strong Search Engine Optimisation** 

The website already achieves an excellent SEO score and uses server-side rendering for the homepage, allowing search engines to index content efficiently. 

#### **Business value** 

- Better organic visibility 

- Lower customer acquisition cost 

- Faster discovery of products 

### **Modern Rendering Architecture** 

The homepage uses Server-Side Rendering followed by client-side hydration. 

#### **Business value** 

- Faster first visual load 

- Better reliability 

- Improved crawlability 

### **Good Accessibility** 

Accessibility is already implemented at a high level. 

#### **Business value** 

- Broader customer reach 

- Reduced legal risk 

- Better usability 

# **Highest Priority Opportunities** 

## **1. Reduce JavaScript Execution** 

### **Business Impact** 

Large JavaScript bundles significantly delay the time before customers can interact with the page. 

This increases abandonment risk, particularly on mobile devices where CPU performance is lower. 

### **Evidence** 

- Approximately **25 MB** of JavaScript downloaded. 

- More than **5 seconds** spent executing JavaScript. 

- Roughly **50%** of downloaded resources remain unused during initial page load. 

### **Business Risk** 

High 

### **Estimated Effort** 

Medium 

### **Recommendation** 

Reduce initial JavaScript payload by: 

- better code splitting 

- lazy loading 

- removing unused dependencies 

## **2. Reduce Third-Party Dependencies** 

### **Business Impact** 

Advertising, analytics, monitoring, and marketing scripts compete with shopping functionality for browser resources. 

Every additional script increases loading time while offering diminishing business value. 

### **Evidence** 

Heavy use of: 

- Google Tag Manager 

- Quantum Metric 

- Facebook 

- Stripe 

- Signifyd 

These collectively consume a significant portion of main-thread execution. 

### **Business Risk** 

High 

### **Estimated Effort** 

Low–Medium 

### **Recommendation** 

Audit third-party services and defer or remove integrations that do not directly improve conversion or operational requirements. 

## **3. Improve Initial Page Weight** 

### **Business Impact** 

Large downloads increase loading time for new visitors and customers on slower networks. 

Slower pages correlate with lower conversion rates. 

### **Evidence** 

- Hundreds of network requests 

- Large overall download size 

- Numerous CSS and JavaScript assets 

### **Business Risk** 

Medium 

### **Estimated Effort** 

Medium 

### **Recommendation** 

Continue optimizing images, CSS delivery, caching strategy, and asset compression. 

## **4. Improve Server Response Time** 

### **Business Impact** 

The initial server response exceeded **800 ms** , delaying the delivery of the first HTML document. 

Although the rendering strategy is appropriate, reducing backend latency would improve perceived responsiveness. 

### **Business Risk** 

Medium 

### **Estimated Effort** 

Medium–High 

### **Recommendation** 

Investigate server-side processing and caching opportunities to reduce Time to First Byte (TTFB). 

# **Priority Matrix** 

**Priority Recommendation Business Effort Impact** 1 Reduce JavaScript execution Very High Medium 2 Audit third-party scripts High Low–Medium 3 Reduce overall page weight Medium Medium 4 Improve server response Medium Medium–High time 

# **Expected Business Benefits** 

Implementing these recommendations is expected to provide: 

- Faster page loading and improved responsiveness. 

- Higher customer satisfaction. 

- Reduced bounce rate. 

- Increased conversion potential. 

- Better mobile shopping experience. 

- Improved Core Web Vitals and long-term SEO performance. 

