<!-- TeamMember.svelte -->
<script>
	/**
	 * @type {{ image: any; name: any; role: any; }}
	 */
	export let member;
</script>

<div class="col-md-3 col-sm-6">
	<div class="our-team">
		<img src={member.image} alt="" />
		<div class="team-content">
			<h3 class="post-title">{member.name}</h3>
			<span class="post">{member.role}</span>
		</div>
	</div>
</div>

<style>
	.our-team {
		position: relative;
		overflow: hidden;
	}
	.our-team img {
		width: 60%;
		height: auto;
	}
	.our-team .team-content {
		width: 100%;
		height: 100%;
		position: absolute;
		top: 0;
		left: 0;
		padding: 45px 18px;
		background: rgba(0, 0, 0, 0.7);
		transform: translateX(-100%);
		transition: all 0.2s ease 0s;
	}
	.our-team:hover .team-content {
		transform: translateX(0);
	}
	.our-team .team-content .post-title {
		font-size: 20px;
		color: #fff;
		text-transform: uppercase;
	}
	.our-team .team-content .post {
		font-size: 20px;
		color: white;
		display: block;
		margin-bottom: 20px;
	}
</style>
