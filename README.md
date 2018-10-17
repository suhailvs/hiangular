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

## check an item in array:

    <div *ngIf="widgets.indexOf('profile') != -1">
    </div>
