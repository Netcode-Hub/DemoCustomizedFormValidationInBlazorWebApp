# Real Time Form Validation in . NET 8 Blazor : Enhancing User Experience While Typing. https://youtu.be/ICyND1SDTwQ
![validate Form b](https://github.com/Netcode-Hub/DemoCustomizedFormValidationInBlazorWebApp/assets/110794348/8ac3e105-966b-403c-96e3-216ccfa35297)

**Install the package**
   
     NetcodeHub.Packages.Components.Validations

**Include the namespace in your project or import.razor file**

     @using NetcodeHub.Packages.Components.Validations.OnInput

**User normal components**

     <EditForm Model="customer" OnValidSubmit="Save" >
    <DataAnnotationsValidator />
    <label class="form-label">ID</label>
    <Number class="form-control mb-2" @bind-Value="customer.Id" />
    <ValidationMessage For="()=>customer.Id"/>

    <label for="fr" class="form-label">Name</label>
    <Text class="form-control mb-2" @bind-Value="customer.Name" id="fr"/>
    <ValidationMessage For="()=>customer.Name" />

    <label class="form-label">ID</label>
    <TextArea class="form-control mb-2" @bind-Value="customer.Address" />
    <ValidationMessage For="()=>customer.Address" />

    <button class="btn btn-primary" type="submit">Save</button>
    </EditForm>


**Using Floating components**
   
    <EditForm Model="customer" OnValidSubmit="Save">
    <DataAnnotationsValidator />
    <FloatingNumber class="form-control mb-2" @bind-Value="customer.Id" Label="ID" Placeholder="eg. 123" id="ty"/>
    <ValidationMessage For="()=>customer.Id" />

    <label class="form-label">Name</label>
    <FloatingText class="form-control mb-2" @bind-Value="customer.Name"  Label="Fullname" Placeholder="John Doe"/>
    <ValidationMessage For="()=>customer.Name" />

    <FloatingTextArea class="form-control mb-2" @bind-Value="customer.Address"  Label="Message" Placeholder="Hello..."/>
    <ValidationMessage For="()=>customer.Address" />

    <button class="btn btn-primary" type="submit">Save</button>
    </EditForm>

    Customer customer = new();
    void Save()
    {

    }
     public class Customer
    {
        [Required, Range(5,100)]
        public int Id { get; set; }
        [Required, MinLength(5), MaxLength(10)]
        public string? Name { get; set; }
        [Required, MinLength(5), MaxLength(15), EmailAddress]
        public string? Email { get; set; }
        [Required, MinLength(5), MaxLength(20), DataType(DataType.MultilineText)]
        public string? Address { get; set; }
    }



/*Follow Netcode-Hub*/ <br/>
https://netcodehub.blogspot.com <br/> 
https://github.com/Netcode-Hub <br/>
https://twitter.com/NetcodeHub | Twitter <br/>
https://web.facebook.com/NetcodeHub | Facebook <br/>
https://www.linkedin.com/in/netcode-hub-90b188258/ | LinkedIn <br/>

/*You can buy a coffee for me to support the channel*/ ☕️ <br/>
https://www.buymeacoffee.com/NetcodeHub <br/>
<a href="https://www.buymeacoffee.com/NetcodeHub" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a> <br/>
PLEASE DO NOT FOGET TO STAR THIS REPOSITORY<br/>
