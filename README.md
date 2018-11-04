# hiangular

## router navigate:

on html::

    <a [routerLink]="['/exammanagement/studentexams/start/', exam.id]"></a>
    
on typescript::

    this.router.navigate(['/exammanagement/studentexams/start/', exam.id]);

you can set `active` class to navbar in Angular2::

    <ul class="nav navbar-nav">
      <li [routerLinkActive]="['active']"> <a [routerLink]="['/exammanagement/studentexams/']">Finished Exams</a></li>
      <li [routerLinkActive]="['active']"> <a [routerLink]="['/exammanagement/upcomingexams/']">Upcoming Exams</a></li>
    </ul>
    
Query Params(pass params in GET)::

    this.router.navigate(['/dashboard/roles/'], {queryParams: { subsubmenu_id: this.subsubmenu_id }});

recive the Query params

    this.subsubmenu_id = this.route.snapshot.queryParamMap.get('subsubmenu_id');
## check an item in array:

    <div *ngIf="widgets.indexOf('profile') != -1">
    </div>

## Loop

**loop an array:**

    let list = [4, 5, 6];

    for (let i in list) {
       console.log(i); // "0", "1", "2",
    }

    for (let i of list) {
       console.log(i); // "4", "5", "6"
    }
    
**loop an object:**

    for (const key of Object.keys(filters)) {
        filters[key] = 'some'
    }
