# Live-Project

## About
For the last two weeks while at The Tech Academy, I worked with a team of colleges on developing a full scale MVC/MVVM Web Application in C#. This project was a great leaning experience that allowed me to create code, fix bugs, clean up previous code, and add multiple features to the project. I worked on several back end stories like creating a modal for people to submit photos, creating different background templates that the user could switch between, and creating a form for people to change email information. Everyone in the team was able to work on both front and back end stories and was able to get skills that will help them all in the future!

### Missing Photo

The missing photo story required me to create a modal that allowed the user to add a photo if one was not placed when creating it initially. Clicking the add photo button will bring up the modal and allow the user to search through their files for a picture to upload and save.


                        <button type="button" class="badge bdge-pill" data-toggle="modal" data-target="#addPhotoModal">Add Photo</button>
                    </span>
                </p>

                <!-- Modal -->
                <div class="modal fade" id="addPhotoModal" role="dialog">
                    <div class="modal-dialog">

                        <!-- Modal content-->
                        <div class="modal-content">
                            <div class="modal-header">
                                <button type="button" class="close" data-dismiss="modal">&times;</button>
                            </div>
                            <div class="modal-body">
                                <div class="col-md-10 formBox">
                                    @*Create a preview image when file is selected*@
                                    <img id="img" alt="" width="100" height="100" />
                                    <input type="file" name="file" class="fileSelect" onchange="document.getElementById('img').src = window.URL.createObjectURL(this.files[0])">
                                </div>
                            </div>
                            <div class="modal-footer">
                                @Html.ActionLink("Add Photo", "CreatePhoto", "Photo", new { id = castMembers.CastMemberID }, new { @class = "badge badge-pill" })
                                <button type="button" class="btn btn-default" data-dismiss="modal">Cancel</button>
                            </div>
                        </div>

                    </div>
                </div>
            }
        }

### Template Background

The template background color change story was to create 3 separate buttons that allowed the user to change the background color scheme of template they were working on.



    <!--Added the buttons to the front of the divs to allign to top right.-->
    <button class="Template-circle-button-Main" onclick="templateColorMain()"></button>
    <button class="Template-circle-button-Main Template-circle-button-Secondary" onclick="templateColorSecondary()"></button>
    <button class="Template-circle-button-Main Template-circle-button-Dark" onclick="templateColorDark()"></button>
    <!--background color turned by Wesley Wojcik-->
    <h4>Templates and Styles Primary</h4>
    



    <!--JonthueM Added regular navbar for easy positioning of buttons in the center of the page-->
    <div @*class="collapse"*@ id="buttonTemplates">
        @*Ryan L commented this out to removed the button*@
        <nav class="navbar navbar-expand-lg mb-4 justify-content-center">
            @*<button class="navbar-toggler admin-dash-collapse-btn" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                  <span class="navbar-toggler-icon admin-dash-collapse-btn-icon"><i class="fas fa-bars"></i> Button Templates</span>
                </button>*@

            <!-- this is Main Color-->

            <ul class="navbar-nav">
                <li class="nav-item">

                    <a class="btn btn-main" href=""><i class="fa fa-edit fa-fw"></i>Edit</a> <!--This button is a link to a different page-->

                </li>
                <li class="nav-item">

                    <a class="btn btn-main" href=""><i class="fa fa-info-circle fa-fw"></i>Details</a> <!--This button is a link to a different page-->

                </li>
                <li class="nav-item">

                    <a class="btn btn-main" href=""><i class="fa fa-trash-alt fa-fw"></i>Delete</a> <!--This button is a link to a different page-->
                    <!-- This demonstrates that multiple buttons can be in the same container-->

                </li>
                <li class="nav-item">

                    <a class="btn btn-main" href=""><i class="fa fa-hand-point-left fa-fw"></i>Back To List</a> <!--This button is a link to a different page-->

                </li>
                <li class="nav-item">

                    <a class="btn btn-main" href=""><i class="fa fa-plus-square fa-fw"></i>Create</a> <!--This button executes the create function-->

                </li>
                <li class="nav-item">

                    <a class="btn btn-main" href=""><i class="fa fa-save fa-fw"></i>Save</a> <!--This button executes the save function-->

                </li>
            </ul>
        </nav>
    </div>

### Change Email Layout

The change email layout was creating and setting up the container for the change email form. 


  <!--
  </div>
    <div class="col-lg-4">
      <div class="">
        @using (Html.BeginForm("ChangeEmail", "Manage", FormMethod.Post, new { @class = "form-horizontal", role = "form" }))
        {
          @Html.AntiForgeryToken()
          @Html.ValidationSummary("", new { @class = "text-danger" })
          <div class="form-group">
            @Html.LabelFor(m => m.OldEmail, new { @class = "control-label" })
            <div class="">
              @Html.TextBoxFor(m => m.OldEmail, new { @class = "form-control" })
            </div>
          </div>
          <div class="form-group">
            @Html.LabelFor(m => m.NewEmail, new { @class = "control-label" })
            <div class="">
              @Html.TextBoxFor(m => m.NewEmail, new { @class = "form-control" })
            </div>
          </div>
          <div class="form-group">
            @Html.LabelFor(m => m.ConfirmEmail, new { @class = "control-label" })
            <div class="">
              @Html.TextBoxFor(m => m.ConfirmEmail, new { @class = "form-control" })
            </div>
          </div>
          <div class="form-group">
            <div class="">
              <button class="iconBtn" type="submit"><i class="fa fa-save fa-fw"></i>Save</button>
            </div>
          </div>
        }
      </div>
    </div> -->
