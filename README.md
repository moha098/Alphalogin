login Form html

<h1 class="header">Login Form</h1>

<div class="loginFormCss">
<div class="row">
    <div class="col-md-6 offset-md-3">
<form class="class-form .bg-info" [formGroup]="loginForm" (ngSubmit)="submit()">
    <div class="mb-4">

    </div>
    <div class="mb-1 ">
    <label>Email:</label>
    </div>
    <div class="mb-2">
    <input type="email" name="email" formControlName="email">
    <div *ngIf="loginForm.get('email')?.touched && !loginForm.get('email')?.valid">
        <span *ngIf="loginForm.get('email')?.errors?.['required']">Email Required</span>
        <span *ngIf="loginForm.get('email')?.errors?.['email']">Enter email in correct format</span>
    </div>
</div>
    <div class="mb-1">
    <label>Password</label>
    </div>
    <div class="mb-3">
    <input type="password" name="password" formControlName="password">
    <div *ngIf=" loginForm.get('password')?.touched && !loginForm.get('password')?.valid">
        <span *ngIf="loginForm.get('password')?.errors?.['required']">Password Required</span>

    </div>
</div>
    <div class="mb-3">
    <button class="btn btn-success" type="submit" [disabled]="!loginForm.valid">Submit</button>
</div>
</form>
</div>
</div>
</div>
