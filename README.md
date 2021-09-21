$(document).ready(function () {
    $("#uploadbutton").click(function () {
        var filename = $("#file").val();

        $.ajax({
            type: "POST",
            url: "addFile.do",
            enctype: 'multipart/form-data',
            data: {
                file: filename
            },
            success: function () {
                alert("Data Uploaded: ");
            }
        });
    });
});
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.0/jquery.min.js"></script>
<span>File</span>
<input type="file" id="file" name="file" size="10"/>
<input id="uploadbutton" type="button" value="Upload"/>
