# Live-Project

## About
For the last two weeks while at The Tech Academy, I worked with a team of colleges on developing a full scale MVC/MVVM Web Application in C#. This project was a great leaning experience that allowed me to create code, fix bugs, clean up previous code, and add multiple features to the project. I worked on several back end stories like creating a modal for people to submit photos, creating different background templates that the user could switch between, and creating a form for people to change email information. Everyone in the team was able to work on both front and back end stories and was able to get skills that will help them all in the future!

### Missing Photo

The missing photo story required me to create a modal that allowed the user to add a photo if one was not placed when creating it initially. Clicking the add photo button will bring up the modal and allow the user to search through their files for a picture to upload and save.

if (Model.models_missing_photos.CastMembers.Count() > 0)
        {
            <p class="h5">Cast Members:</p>
            foreach (var castMembers in (List<TheatreCMS.Models.CastMember>)ViewData["CastMembersWithoutPhotos"])
            {
                <p class="dashboard-subsection">
                    @castMembers.Name
                    <span class="dashboard-badges mx-3">
                        @Html.ActionLink("Edit", "Edit", "CastMembers", new { id = castMembers.CastMemberID }, new { @class = "badge badge-pill" }) |
                        @Html.ActionLink("Delete", "Delete", "CastMembers", new { id = castMembers.CastMemberID }, new { @class = "badge badge-pill" })


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
