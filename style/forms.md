# Forms

#### Links
- https://developer.mozilla.org/en/docs/Web/HTML/Element/Input
- http://html5doctor.com/html5-forms-input-types/
- http://alistapart.com/article/forward-thinking-form-validation
- http://www.wufoo.com/html5/
- http://html5doctor.com/css3-pseudo-classes-and-html5-forms/
- http://html5doctor.com/html5-forms-introduction-and-new-attributes/
- http://www.broken-links.com/2011/06/16/styling-html5-form-validation-errors/

**Flexbox**
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes
- https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- http://www.smashingmagazine.com/2015/03/harnessing-flexbox-for-todays-web-apps/
- http://www.sketchingwithcss.com/samplechapter/cheatsheet.html
- https://developer.mozilla.org/en-US/docs/Web/CSS/align-content

```html
  <!-- ======================================
   # Overall form structure
   ====================================== -->  
  <form autocomplete="on">
    <fieldset>
      <legend>Fieldset title</legend>

      <!-- ....fieldset items -->
    </fieldset>
    <div> <!-- Form actions -->
      <button type="submit" autocomplete="off"></button> <!-- See: https://bugzilla.mozilla.org/show_bug.cgi?id=654072 and https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button -->
      <button type="reset" autocomplete="off"></button>
    </div>
  </form>

  <!-- ======================================
   # Basic item format
   ====================================== -->
    <!-- Simple item format -->
    <label>
      <input title"Label text" type="">
      <span>Label text</span>
    </label>

    <!-- 'Required' item format -->
    <!-- CSS: [required] ~ span:before { /* Add an indicator */ } -->
    <label>
      <input title"Label text" type="" required>
      <span>Label text</span>
    </label>

    <!-- OR (Prefer previous) -->
    <label>
      <input title"Label text" type="" required>
      <span>Label text</span>
      <abbr title="required">*</abbr>
    </label>


  <!-- ======================================
   # Input types
   ====================================== -->
    <!--
     * Attributes worth considering:
     * - autofocus (!! BEWARE - UX !!)
     * - inputmode (not supported yet - hints to keyboard)
     * - multiple
     * - pattern
     * - placeholder
     *   (CSS: -mozplaceholder and –webkit-input-placeholder to style)
     * - required (see: http://www.broken-links.com/2011/06/16/styling-html5-form-validation-errors/)
     *
     -->

    <!-- Ready -->
    <input type="checkbox">
    <input type="email">
    <input type="file"> <!-- ? -->
    <input type="password">
    <input type="reset"> <!-- !Button preferred to input -->
    <input type="radio">
    <input type="search">
    <input type="tel">
    <input type="text">
    <input type="url">

    <!-- Under consideration -->
    <!-- <input type="number" min="5" max="18" step="0.5"> --> <!-- DON'T USE - Unpredictable behaviour and 'spinner' in some browsers -->
    <!-- <input type="range" min="1" max="100" value="0"> --> <!-- Can we control style/render -->

    <!-- Not ready -->
    <!-- <input type="color"> -->
    <!-- <input type="date" min="2010-01-01" max="2100-01-01"> -->
    <!-- <input type="datetime"> -->
    <!-- <input type="datetime-local"> -->
    <!-- <input type="month"> -->
    <!-- <input type="time"> -->
    <!-- <input type="week"> -->


  <!-- ======================================
   # HTML Constructs
   ====================================== -->
    <!-- Toggle -->
    <label>
      <input type="">
      <span>Label</span>
      <span><!-- faux --></span>
    </label>


    <!-- Checkbox -->
    <label>
      <input type="">
      <span>Label</span>
      <span><!-- faux --></span>
    </label>


    <!-- Checkbox list -->
    <fieldset>
      <legend>Checkbox list</legend>
      <label>
        <input type="">
        <span>Label</span>
        <span><!-- faux --></span>
      </label>
      <label>
        <input type="">
        <span>Label</span>
        <span><!-- faux --></span>
      </label>
    </fieldset>
    <!-- OR -->
    <fieldset>
      <legend>Checkbox list</legend>
      <div>
        <label>
          <input type="">
          <span>Label</span>
          <span><!-- faux --></span>
        </label>
        <label>
          <input type="">
          <span>Label</span>
          <span><!-- faux --></span>
        </label>
      </div>
    </fieldset>


    <!-- Radio buttons -->
    <fieldset>
      <legend>Radio button list</legend>
      <label>
        <input type="" name="rb2">
        <span>Label</span>
        <span><!-- faux --></span>
      </label>
      <label>
        <input type="" name="rb2">
        <span>Label</span>
        <span><!-- faux --></span>
      </label>
    <legend>
    <!-- OR -->
    <fieldset>
      <legend>Radio button list</legend>
      <div>
        <label>
          <input type="" name="rb2">
          <span>Label</span>
          <span><!-- faux --></span>
        </label>
        <label>
          <input type="" name="rb2">
          <span>Label</span>
          <span><!-- faux --></span>
        </label>
      </div>
    <fieldset>

    <!-- Select list -->
    <label>
      <span>Label</span>
      <div>
        <select>
          <option></option>
          <option selected></option>
          <option></option>
          <option></option>
        </select>
      </div>
    </label>


    <!-- Textarea -->
    <label>
      <textarea></textarea>
      <span>Label</span>
    </label>


    <!-- Form actions -->
    <div>
      <button type="submit" autocomplete="off"></button>
      <button type="reset" autocomplete="off"></button>
      <!-- OR -->
      <input type="submit"></input>
      <input type="reset"></input>
    </div>


    <!-- Datalist -->
    <datalist id="my-datalist">
      <option></option>
      <option></option>
      <option></option>
    </datalist>

    <!-- Datalist : Assignment -->
    <input type="text" list="my-datalist" multiple>

    <label>
      <input type="text" list="my-other-datalist" multiple>
      <span>Label</span>
      <datalist id="my-other-datalist">
        <option></option>
        <option></option>
        <option></option>
      </datalist>
    </label>

```
