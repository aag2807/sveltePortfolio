<script>

</script>

<style lang="scss">



// VARIABLES
$mainblack: #22262b;
$amain: #fbb053;
$grisclaro: #e0e2e2;
$display: #abadc6;
$item: #d1c9bf;
$codred: #ac5e47;

// MISC
.wrap{
	width: 100%;
	height: 55vh;
	position: relative;
	background-color: $mainblack;
	display: flex;
	justify-content: center;
	align-items: center;
	display:flex;
	flex-direction: column;
	justify-content: center;
}
.comp{
    width: 100%;
    height: 194px;
    text-align: center;
    .monitor{
		width: 275px;
		height: 181px;
		display: block;
		margin: 0 auto;
		border-radius: 10px 10px 0px 0px;
		padding: 9px;
		border: solid 1px $grisclaro;
		background-color: black;
    }
    .mid{
    	float: left;
    	display: block;
    	height: 100%;
    	position: relative;
    	background-color: $display;
    	width: 50%;
    	&.codigo{
    		background-color: $mainblack;
    	}
    }
    .site{
    	overflow: hidden;
    	position: absolute;
		width: 105px;
		height: 138px;
	    bottom: 0;
	    right: 0;
    	.topbar{
			width: 100%;

    	}
    	.cerrar{
			width: 100%;
			padding: 3px;
			line-height: 0;
			display: flex;
		    align-items: center;
		    justify-content: flex-start;
		    border-radius: 4px 4px 0px 0px;
			background-color: #afa895;
			&>div{
				display: inline-block;
				width: 2px;
				height: 2px;
				border-radius: 50%;
				background: white;
				margin: 0px 1px;
			}
		}
		.inhead{
			padding: 2px;
			height: 5px;
			background-color: #ddd8cf;
			.item{
				width: 10px;
    			height: 1px;
				background-color: $item;
				margin: 0 1px;
				display: block;
				float: left;
			}
		}
    }
    .txr{
    	text-align: right;
		.item{
			float: right;
		}
    }
    .inslid{
    	width: 100%;
    	height: 33px;
    	background-color: #efebe2;
    }
    .incont{
		padding-top: 10px;
		background: #fefaf0;
    	.item{
			background-color: $item;
			width: 53px;
			height: 2px;
			display: block;
			margin: 0 auto;
			margin-top: 1px;
			&:nth-child(1){
				width: 20px;
			}
			&:nth-child(2){
				margin-top: 3px;
				width: 41px;
			}
			&:nth-child(3){
				width: 32px;
			}
			&:nth-child(4){
				width: 23px;
			}
    	}
    	.wid{
    		width: 100%;
    		padding: 8px 1px;
    		.itwid{
    			width: 33.333%;
    			float: left;
    			height: 26px;
    			padding: 0px 3px;
    			&>div{
    				width: 100%;
    				height: 100%;
    				background-color: #f5f1e6;
    				position: relative;
    				.contfoot{
    					position: absolute;
    					bottom: 0;
    					left: 0;
    					height: 6px;
    					width: 100%;
    					background-color: #ebe5dc;
    				}
    			}
    		}
    	}
    	.infoot{
    		background-color: #efebe2;
    		height: 26px;
    		width: 100%;
    	}
    }
	@keyframes code {
	    0% {
			opacity: 1;
	    }
	    50% {
			opacity: 0.6;
	    }
	    100% {
			opacity: 1;
	    }
	}
    .codigo{
    	padding: 14px 0px 14px 14px;
    	.var{
    		background-color: $codred;
	    	animation: code;
			animation-duration: 0.3s;
			animation-iteration-count: infinite;
    	}
    	.cont{
    		background-color: #464748;
	    	animation: code;
			animation-duration: 0.5s;
			animation-iteration-count: infinite;
    	}
    	.fun{
    		background-color: $amain;
	    	animation: code;
			animation-duration: 0.2s;
			animation-iteration-count: infinite;
    	}
    	.atr{
    		background-color: #645572;
	    	animation: code;
			animation-duration: 0.1s;
			animation-iteration-count: infinite;
    	}
    	.item{
    		height: 3px;
    		width: 20px;
    		float: left;
    		margin-right: 3px;
    		&.min{
    			width: 13px;
    		}
    		&.lrg{
    			width: 30px;
    		}
    	}
    	.line{
    		padding: 2px 0;
    		width: 100%;
    	}
    	.tab1{
    		padding-left: 5px;
    	}
    	.tab2{
    		padding-left: 8px;
    	}
    	.tab3{
    		padding-left: 10px;
    	}
    	.tab4{
    		padding-left: 12px;
    	}
    }
}

.base {
    width: 338px;
    height: 12px;
    background: $grisclaro;
    display: block;
    margin: 0 auto;
    border-radius: 0px 0px 6px 6px;
}  



.one {
	color: #d65a31;
}
.two{
	color: #673ab7;
}

#parent {
  height: 40px;
  white-space: nowrap;
  overflow: hidden; 
  font-family: 'Source Code Pro', monospace;  
  font-size: 28px;
  color: rgba(255,255,255,.70);
  position: relative;
}

#border {
  border-bottom: solid 3px rgba(0,255,0,.75);
  position: absolute;
  right: -7px;
  width: 20px;
}

/* Animation */
#parent {
  animation: animated-text 2s steps(30,end) 1s 1 normal both
}

#border {
   animation: animated-cursor 600ms steps(30,end) infinite;
}

/* text animation */

@keyframes animated-text{
  from{width: 0;}
  to{width: 480px;}
}

/* cursor animations */

@keyframes animated-cursor{
  from{border-bottom-color: rgba(0,255,0,.75);}
  to{border-bottom-color: transparent;}
}
</style>


<div class="wrap pb-6 mb-6">
	<div class='text-center mt-0 mb-2'>
		<h5 class="text-h5 white-text">Alvaro Guzman</h5>
		<div id="parent">
			<span class="one">Full</span>-<span class="two">Stack</span> Programmer<div id="border"></div></div>
	</div>
	<div class="comp pt-4">
		<div class="monitor">
			<div class="mid">
				<div class="site">
					<div class="topbar">
						<div class="cerrar">
							<div class="circl" />
							<div class="circl" />
							<div class="circl" />
						</div>
					</div>
					<div class="inhead">
						<div class="mid">
							<div class="item" />
						</div>
						<div class="mid txr">
							<div class="item" />
							<div class="item" />
							<div class="item" />
							<div class="item" />
						</div>
					</div>
					<div class="inslid" />
					<div class="incont">
						<div class="item" />
						<div class="item" />
						<div class="item" />
						<div class="item" />
						<div class="wid">
							<div class="itwid">
								<div>
									<div class="contfoot" />
								</div>
							</div>
							<div class="itwid">
								<div>
									<div class="contfoot" />
								</div>
							</div>
							<div class="itwid">
								<div>
									<div class="contfoot" />
								</div>
							</div>
							<div class="clearfix" />
						</div>
						<div class="infoot" />
					</div>
				</div>
			</div>
			<div class="mid codigo">
				<div class="line">
					<div class="item var" />
					<div class="item cont" />
					<div class="clearfix" />
				</div>
				<div class="line">
					<div class="item min var" />
					<div class="item min fun" />
					<div class="clearfix" />
				</div>
				<div class="line">
					<div class="item min var" />
					<div class="clearfix" />
				</div>
				<div class="line">
					<div class="item var" />
					<div class="item atr" />
					<div class="item cont" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item min atr" />
					<div class="item lrg fun" />
					<div class="item min fun" />
					<div class="item lrg cont" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item lrg atr" />
					<div class="item min fun" />
					<div class="item min cont" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item atr" />
					<div class="item min fun" />
					<div class="item atr" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item min atr" />
					<div class="item min cont" />
					<div class="item lrg atr" />
					<div class="item  fun" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item min atr" />
					<div class="item lrg fun" />
					<div class="item lrg cont" />
					<div class="item min fun" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item min var" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item min var" />
					<div class="clearfix" />
				</div>
				<div class="line tab2">
					<div class="item min var" />
					<div class="clearfix" />
				</div>
				<div class="line tab2">
					<div class="item min atr" />
					<div class="item min fun" />
					<div class="clearfix" />
				</div>
				<div class="line tab3">
					<div class="item min atr" />
					<div class="item min fun" />
					<div class="item lrg fun" />
					<div class="item lrg cont" />
					<div class="clearfix" />
				</div>
				<div class="line tab3">
					<div class="item min atr" />
					<div class="item min fun" />
					<div class="item lrg atr" />
					<div class="item lrg cont" />
					<div class="clearfix" />
				</div>
				<div class="line tab4">
					<div class="item min fun" />
					<div class="item lrg atr" />
					<div class="clearfix" />
				</div>
				<div class="line tab1">
					<div class="item atr" />
					<div class="item var" />
					<div class="item cont" />
					<div class="clearfix" />
				</div>
				<div class="line tab3">
					<div class="item min var" />
					<div class="clearfix" />
				</div>
				<div class="line tab4">
					<div class="item min atr" />
					<div class="item min fun" />
					<div class="item lrg atr" />
					<div class="item lrg cont" />
					<div class="clearfix" />
				</div>
				<div class="line">
					<div class="item min var" />
					<div class="clearfix" />
				</div>
			</div>
		</div>
		<div class="base" />
	</div>
</div>
