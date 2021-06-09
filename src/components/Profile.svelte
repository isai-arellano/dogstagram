<script>
  export let nickname;
  export let name;
</script>
<style>
    .Profile-content {
      display: flex;
      align-items: center;
    }
    .Profile-avatar img {
      width: 42px;
      height: 42px;
      border-radius: 50%;
    }
    .Profile-info {
      margin: 0 0 0 0.5em;
    }
    .Profile-info h2 {
      font-size: 14px;
      color: black;
      margin: 0;
      padding: 0;
    }
    .Profile-info span {
      font-size: 12px;
      font-weight: normal;
    }
  </style>
  
<div class="Profile">
    <div class="Profile-content">
        <div class="Profile-avatar">
            <img src="https://firebasestorage.googleapis.com/v0/b/dogstagram-90148.appspot.com/o/PHOTO-2021-05-17-13-03-34.jpg?alt=media&token=68c68f6a-b99c-4386-92b2-ce282dd3639d" alt=""/>
        </div>
        <div class="Profile-info">
            <h2>{nickname}</h2>
            <span>{name}</span>
        </div>
    </div>
</div>