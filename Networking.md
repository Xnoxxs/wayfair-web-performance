# **Networking Baseline – Wayfair Homepage** 

## **1. How many requests are made?** 

During the initial page load, the homepage makes **771 network requests** and finishes loading in approximately **6.3 seconds** . This is a relatively high number and suggests that the page relies on many different resources, including images, JavaScript files, stylesheets, fonts, third-party services, and API requests. 

## **2. How much data is transferred? What is the total resource size? What is the compression reduction?** 

During the initial (hard) reload: 

- **Requests:** 771 

- **Transferred:** 8.2 MB 

- **Total Resources:** 72.2 MB 

- **Load Time:** 6.3 seconds 

The browser transfers **8.2 MB** of data over the network while loading resources with a combined size of approximately **72.2 MB** . This indicates that the website benefits from optimization techniques such as HTTP compression and efficient resource delivery, reducing the amount of data that needs to be downloaded. 

The response headers also show that JavaScript files are compressed using **gzip** , which further reduces the amount of data transferred over the network. 

## **3. How much data is transferred on a soft refresh? What is the reduction due to caching?** 

During a normal (soft) refresh: 

- **Requests:** 628 

- **Transferred:** 635 kB 

- **Total Resources:** 92.3 MB 

- **Load Time:** 5.4 seconds 

Compared to the initial transfer of **8.2 MB** , only **635 kB** needs to be downloaded on a soft refresh. This is a reduction of approximately **7.6 MB** , or about **92% less transferred data** . 

This demonstrates that browser caching is working effectively, allowing many previously downloaded resources to be reused instead of being downloaded again. 

## **4. How much of the data is JavaScript/CSS vs Images? Are these compressed?** 

|**Resource**|**Request**|**Resource Size**|
|---|---|---|
|**Type**|**s**||
|JavaScript|206|24,975 kB (~25.0 MB)|
|CSS|35|2,197 kB (~2.2 MB)|
|Images|67|1,037 kB (~1.0 MB)|



**Total Resource Size:** 70,453 kB (~70.5 MB) 

### **Approximate Breakdown** 

- **JavaScript:** ~25.0 MB (≈35% of all resources) 

- **CSS:** ~2.2 MB (≈3%) 

- **Images:** ~1.0 MB (≈1.5%) 

The remaining resources consist of HTML, fonts, third-party scripts, API responses, tracking resources, and other assets. 

The homepage relies heavily on **JavaScript** . The measurements were taken after a **soft refresh** , so many resources had already been loaded from the browser cache. Even so, JavaScript still represents the largest category of resources used by the page. 

JavaScript is responsible for many of the site's interactive features, including search, recommendations, personalization, analytics, and shopping functionality. 

The response headers show that JavaScript files are compressed using **gzip** , helping reduce the amount of data transferred over the network. The image resources are primarily **PNG** and 

**GIF** files, which are already compressed image formats and therefore are generally not compressed further using HTTP compression. 

# **Additional Findings** 

## **Finding 1 – Very High Number of Network Requests** 

The homepage loads many different resources, including images, JavaScript files, stylesheets, fonts, API requests, and third-party services, resulting in **771 network requests** during the initial page load. 

### **How does this affect users?** 

Making hundreds of requests increases the amount of work the browser must perform before the page is fully loaded. Each request adds network overhead and can increase loading time, particularly on slower internet connections. 

### **Which metric(s) are being affected?** 

- Overall page load time 

- Network latency 

- Speed Index 

### **What is the solution, or a likely solution?** 

Reduce unnecessary requests by removing unused assets, combining small files where appropriate, and delaying non-essential resources until after the initial page load. 

## **Finding 2 – Large Initial Data Transfer** 

The homepage contains many JavaScript files, images, third-party resources, and other assets that contribute to an **8.2 MB** network transfer during the initial visit. 

### **How does this affect users?** 

Downloading **8.2 MB** of data during the first visit increases loading times, especially for users on slower internet connections or limited mobile data plans. 

### **Which metric(s) are being affected?** 

- Largest Contentful Paint (LCP) 

- Speed Index 

- Overall Performance 

### **What is the solution, or a likely solution?** 

Reduce the size of images, optimize JavaScript bundles, remove unused resources, and continue using modern compression techniques to decrease the amount of data transferred. 

## **Finding 3 – Heavy Reliance on JavaScript** 

The homepage relies heavily on JavaScript to support search, recommendations, personalization, analytics, shopping functionality, and other interactive features. 

### **How does this affect users?** 

Large amounts of JavaScript increase the time required before the page becomes fully interactive. Users may experience delays when scrolling, clicking buttons, or interacting with the website. 

### **Which metric(s) are being affected?** 

- Total Blocking Time (TBT) 

- Interaction responsiveness 

- Overall Performance 

### **What is the solution, or a likely solution?** 

Reduce unused JavaScript, split large bundles into smaller chunks, and defer scripts that are not immediately required for the initial page load. 

## **Finding 4 – Effective Browser Caching** 

Browser caching appears to be working effectively, as shown by the reduction in transferred data from **8.2 MB** on a hard refresh to **635 kB** on a normal refresh. This indicates that many previously downloaded resources are being reused instead of downloaded again. 

### **How does this affect users?** 

Returning visitors experience significantly faster page loads because many resources are loaded directly from the browser cache instead of being downloaded again. 

### **Which metric(s) are being affected?** 

- Repeat page load time 

- Network usage 

- Overall user experience 

