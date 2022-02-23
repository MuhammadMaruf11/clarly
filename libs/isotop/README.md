# Isotop Filter

- https://isotope.metafizzy.co/


## Documentation

- https://isotope.metafizzy.co/filtering.html


## Html Markup

```html
<!-- filter-wrapper start -->
<div class="filter-wrapper">
    <!-- filter-nav start -->
    <div class="filter-nav">
        <button class="active" data-filter="*">All</button>
        <button data-filter=".tab1">tab 1</button>
        <button data-filter=".tab2">tab 2</button>
        <button data-filter=".tab3">tab 3</button>
        <button data-filter=".tab4">tab 4</button>
    </div>
    <!-- filter-nav end -->

    <!-- filter-grid start -->
    <div class="filter-grid row">

        <!-- grid-item start -->
        <div class="col-xl-4 grid-item tab1">
            <h1>Heading 1</h1>
        </div>
        <!-- grid-item end -->

        <!-- grid-item start -->
        <div class="col-xl-4 grid-item tab2">
            <h1>Heading 2</h1>
        </div>
        <!-- grid-item end -->

        <!-- grid-item start -->
        <div class="col-xl-4 grid-item tab3">
            <h1>Heading 3</h1>
        </div>
        <!-- grid-item end -->

        <!-- grid-item start -->
        <div class="col-xl-4 grid-item tab4">
            <h1>Heading 4</h1>
        </div>
        <!-- grid-item end -->

        <!-- grid-item start -->
        <div class="col-xl-4 grid-item tab1">
            <h1>Heading 1</h1>
        </div>
        <!-- grid-item end -->

    </div>
    <!-- filter-grid end -->
</div>
<!-- filter-wrapper end -->

```

## Js Code

```js

if (jQuery(".filter-wrapper").length > 0) {
    $('.filter-wrapper .filter-grid').imagesLoaded(function () {
        let $grid = $('.filter-wrapper .class-filter-grid').isotope({
            itemSelector: '.grid-item',
            percentPosition: true,
            layoutMode: 'fitRows',
            masonry: {
                columnWidth: '.grid-item' // columnWidth: 1
            }
        });

        // filter items on button click
        $('.filter-wrapper .filter-nav').on('click', 'button', function () {
            let filterValue = $(this).attr('data-filter');
            $grid.isotope({filter: filterValue});
        });

        //for menu active class
        $('.filter-wrapper .filter-nav button').on('click', function (event) {
            $(this).siblings('.active').removeClass('active');
            $(this).addClass('active');
            event.preventDefault();
        });

    });
}

```

## if use bootstrap tab with filter

```js

// fix tabs
$('a[data-toggle="tab"]').on('shown.bs.tab', function (e) {
    $grid.isotope('layout');
});

```
