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

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

Login Form CSS
span{
    color:red
}

.header{
    text-align: center;
    background-color: black;
    color:lightsteelblue ;
    font-family: cursive;
    
}

.loginFormCss{
    background-color:lightsteelblue;
    position:absolute;
    top:20%;
    left:20%;
    right:20%;
    height:250px;

}

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

LoginForm Ts file

 loginForm:FormGroup
  constructor(private fb:FormBuilder){
    this.loginForm=this.fb.group({
      email:['',[Validators.required]],
      password:['',[Validators.required]]
    })
  }

  submit(){
    console.log(this.loginForm.value)
  }

//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

Signup Form html

<h1 class="header">Signup Form</h1>

<div class="loginFormCss">
<div class="row">
    <div class="col-md-6 offset-md-3">
<form class="class-form .bg-info" [formGroup]="signupForm" (ngSubmit)="submit()">
    <div class="mb-4">

    </div>
    <div class="mb-1 ">
    <label>Email:</label>
    </div>
    <div class="mb-2">
    <input type="email" name="email" formControlName="email">
    <div *ngIf="signupForm.get('email')?.touched && !signupForm.get('email')?.valid">
        <span *ngIf="signupForm.get('email')?.errors?.['required']">Email Required</span>
        <span *ngIf="signupForm.get('email')?.errors?.['email']">Enter email in correct format</span>
    </div>
</div>
    <div class="mb-1">
    <label>Password</label>
    </div>
    <div class="mb-3">
    <input type="password" name="password" formControlName="password">
    <div *ngIf=" signupForm.get('password')?.touched && !signupForm.get('password')?.valid">
        <span *ngIf="signupForm.get('password')?.errors?.['required']">Password Required</span>

    </div>
</div>
    <div class="mb-3">
    <button class="btn btn-success" type="submit" [disabled]="!signupForm.valid">Submit</button>
</div>
</form>
</div>
</div>
</div>

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

SignupForm Css

span{
    color:red
}

.header{
    text-align: center;
    background-color: black;
    color:lightsteelblue ;
    font-family: cursive;
    
}

.loginFormCss{
    background-color:lightsteelblue;
    position:absolute;
    top:20%;
    left:20%;
    right:20%;
    height:250px;

}

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

signup form ts


 signupForm:FormGroup
  constructor(private fb:FormBuilder){
    this.signupForm=this.fb.group({
      email:["",[Validators.required]],
      password:["",[Validators.required]]
    })
  }

  submit(){
    console.log(this.signupForm.value)
  }
  /////////////////////////////////////////////////////////////////////////////







