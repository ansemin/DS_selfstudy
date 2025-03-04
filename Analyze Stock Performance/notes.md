# 1. HTML for webscrapping 


1. **HTML Basics**:
   - HTML (Hypertext Markup Language) is used to structure content on web pages.
   - Tags (e.g., `<html>`, `<head>`, `<body>`) define how content is displayed in a browser.
   - The `<html>` element is the root of an HTML document, containing `<head>` (meta-information) and `<body>` (visible content).

2. **HTML Tags and Structure**:
   - Tags consist of a tag name (e.g., `<h3>`, `<p>`, `<a>`), attributes (e.g., `href` in `<a>`), and content enclosed between opening (`<tag>`) and closing (`</tag>`) tags.
   - Example: `<a href="https://www.ibm.com">IBM</a>` creates a hyperlink to IBM's website.

3. **HTML Document as a Tree**:
   - HTML documents can be visualized as a **tree structure**:
     - Parent-child relationships exist between tags (e.g., `<html>` is the parent of `<head>` and `<body>`).
     - Sibling tags are at the same level (e.g., `<head>` and `<body>` are siblings).
     - Descendants include all nested tags within a parent tag.

4. **HTML Tables**:
   - Tables are defined using `<table>`, with rows (`<tr>`), headers (`<th>`), and cells (`<td>`).
   - Example structure:
     ```html
     <table>
       <tr>
         <th>Header 1</th>
         <th>Header 2</th>
       </tr>
       <tr>
         <td>Row 1, Cell 1</td>
         <td>Row 1, Cell 2</td>
       </tr>
     </table>
     ```

5. **Web Scraping Context**:
   - Data of interest (e.g., player names and salaries) is often embedded within specific HTML tags (e.g., `<h3>` for names, `<p>` for salaries).
   - Understanding HTML structure is crucial for identifying and extracting relevant data programmatically.

6. **Practical Application**:
   - Tools like browser inspectors help analyze HTML elements.
   - Python can be used to parse HTML trees and extract data systematically.


# 2. Web Scrapping 

The key tools used are the **Requests** library to download the webpage and **BeautifulSoup** to parse and navigate the HTML structure.

Key points covered:
1. **BeautifulSoup Objects**: These represent the HTML document as a nested tree structure, allowing you to navigate and extract specific elements (e.g., tags, attributes, text).
   - Tags can be accessed like tree nodes, with methods to navigate up (parent), down (child), or sideways (siblings).
   - Attributes of tags can be accessed like dictionary key-value pairs.
2. **`find_all` Method**: This method filters and retrieves all elements matching specific criteria (e.g., tag names, attributes). It returns an iterable list of tag objects.
   - Example: Extracting rows (`<tr>`) and cells (`<td>`) from an HTML table.
3. **Web Scraping Workflow**:
   - Use the `requests.get()` method to fetch the webpage content.
   - Parse the HTML content into a BeautifulSoup object.
   - Use BeautifulSoup methods like `find_all` to extract desired data.

**Main takeaway**: Web scraping with Python (using Requests and BeautifulSoup) enables efficient extraction and analysis of data from websites, transforming overwhelming manual tasks into streamlined automated processes.
