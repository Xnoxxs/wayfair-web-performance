# **Finding 1 – Large Images Slow Down Page Loading** 

## **What is the cause, or most likely cause?** 

The report shows that many images are larger than necessary and could be compressed further. It also identifies an estimated saving of **1,596 KiB** by improving image delivery. Several images are downloaded at much larger resolutions than they are displayed on the page. 

## **How does this affect users?** 

Large images take longer to download, especially on slower internet connections. Users have to wait longer before the most important content becomes visible, making the website feel slower and less responsive. This can increase the chances of users leaving the page before it fully loads. 

## **Which metric(s) are being affected?** 

- Largest Contentful Paint (LCP) 

- Speed Index 

- Overall Performance Score 

## **What is the solution, or a likely solution?** 

Compress images further, serve them in modern formats such as WebP or AVIF, and use responsive images so that users only download the image size needed for their device. 

# **Finding 2 – Very High Total Blocking Time** 

## **What is the cause, or most likely cause?** 

The Total Blocking Time is **6,660 ms** , which is extremely high. This suggests that the browser is spending a long time executing JavaScript on the main thread before becoming fully interactive. 

## **How does this affect users?** 

Although some content appears quickly, the page remains busy processing JavaScript before it can fully respond to user interactions. This can make clicking buttons, opening menus, or scrolling feel delayed and unresponsive. 

## **Which metric(s) are being affected?** 

- Total Blocking Time (TBT) 

- Overall Performance Score 

## **What is the solution, or a likely solution?** 

Reduce the amount of JavaScript loaded on the initial page, remove unused code, split large JavaScript bundles into smaller files, and defer non-essential scripts until after the page becomes interactive. 

# **Finding 3 – Browser Caching Could Be Improved** 

## **What is the cause, or most likely cause?** 

The report recommends using more efficient cache lifetimes and estimates that around **1,128 KiB** of data could be saved by improving caching policies. 

## **How does this affect users?** 

Returning visitors have to download many of the same files again instead of loading them from the browser cache. This increases loading times and uses more network bandwidth than necessary. 

## **Which metric(s) are being affected?** 

- Speed Index 

- Largest Contentful Paint (LCP) 

- Overall Performance Score 

## **What is the solution, or a likely solution?** 

Configure longer cache lifetimes for static assets such as images, CSS, JavaScript, and fonts so that repeat visitors do not need to download them again. 

# **Finding 4 – Images Are Not Responsive** 

## **What is the cause, or most likely cause?** 

The report shows multiple examples where images are served at resolutions much larger than their displayed dimensions, resulting in unnecessary downloads. 

## **How does this affect users?** 

Users download images that are much larger than the size at which they are displayed. This increases page weight and slows down loading, particularly on mobile devices and slower internet connections. 

## **Which metric(s) are being affected?** 

- Largest Contentful Paint (LCP) 

- Speed Index 

- Overall Performance Score 

## **What is the solution, or a likely solution?** 

Use responsive images with the srcset and sizes attributes so browsers download the most appropriate image size for each screen. 

# **Finding 5 – Large JavaScript Files Increase Processing Time** 

## **What is the cause, or most likely cause?** 

The report identifies several JavaScript bundles that are hundreds of kilobytes in size and contribute significantly to main-thread processing time. These large files increase the amount of JavaScript the browser must download, parse, and execute before the page becomes fully interactive. 

## **How does this affect users?** 

Large JavaScript files increase the amount of work the browser has to do before the page becomes fully usable. Even if the page is visible, users may notice delays when interacting with it. 

## **Which metric(s) are being affected?** 

- Total Blocking Time (TBT) 

- Speed Index 

- Overall Performance Score 

## **What is the solution, or a likely solution?** 

Reduce unused JavaScript, split large bundles into smaller chunks, load non-essential code only when needed, and defer scripts that are not required during the initial page load. 

