<template>
<div>
    <div class="row">
        <div class="col-12">
        <div class="card">
            <div class="card-header">
                <h3 class="card-title">
                    <i class="fa fa-fw ti-check-box"></i> Multiple Select with Search Option
                </h3>
                <span class="float-right txt_font">
                    <i class="fa fa-fw ti-angle-up clickable"></i>
                    <i class="fa fa-fw ti-close removecard"></i>
                </span>
            </div>
            <div class="card-body">
                <div class="row">
                    <div class="col-sm-12 col-md-12 col-lg-12">
                        <input type="search" class="form-control" id="search" placeholder="Add your options.." v-model="search" >
                    </div>
                    <div class="col-12 col-sm-6 col-md-4" v-for="drink in allDrinks">
                        <div class="pull-left">
                            <i class="fa fa-tags" ></i>
                        </div>
                        <div class="searchable-container">
                            <div data-toggle="buttons" class="btn-group bizmoduleselect"  >
                                <label class="btn btn-secondary" :class="{ active: drink.active}" @click="drink.active=!drink.active">
                                    <div class="bizcontent">
                                        <input type="checkbox" name="var_id[]" autocomplete="off" value="" @click.stop.prevent>
                                        <i class="fa" :class="{'fa-check':drink.active}"></i>
                                        <h5>{{drink.name}}</h5>
                                    </div>
                                </label>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        </div>
    </div>
    <div class="row">
        <div class="col-md-6">
            <div class="card ">
                <div class="card-header">
                    <h3 class="card-title">
                        <i class="fa fa-fw ti-check-box"></i> Labelauty Radio and Checkboxes
                    </h3>
                    <span class="float-right txt_font">
                        <i class="fa fa-fw ti-angle-up clickable"></i>
                        <i class="fa fa-fw ti-close removecard"></i>
                    </span>
                </div>
                <div class="card-body" id="lby-content">
                    <div class="row" id="lby-demo">

                        <div class="col-lg-6 col-md-12 col-sm-6">
                            <h5>Labeled Checkboxes</h5>
                            <input class="to-labelauty synch-icon1" data-labelauty="Unselected|Australia"
                                   type="checkbox" checked/>
                            <input class="to-labelauty terms-icon" type="checkbox"
                                   data-labelauty="Unselected|Selected"/>
                            <input class="to-labelauty synch-icon" type="checkbox"
                                   data-labelauty="I am disabled!" disabled/>
                        </div>
                        <div class="col-lg-6 col-md-12 col-sm-6">
                            <h5>Non-labeled Check</h5>
                            <input class="to-labelauty-icon check-icon" type="checkbox" checked/>
                            <input class="to-labelauty-icon check-icon" type="checkbox"/>
                            <input class="to-labelauty-icon check-icon" type="checkbox" disabled checked/>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-lg-6 col-md-12 col-sm-6">
                            <h5>Labeled Radio Buttons</h5>
                            <input class="to-labelauty synch-icon2" type="radio" name="rd2"
                                   data-labelauty="Unselected|USA"/>
                            <input class="to-labelauty terms-icon" type="radio" name="rd2"
                                   data-labelauty="Unselected|Selected" checked/>
                            <input class="to-labelauty synch-icon" type="radio" name="rd3" disabled
                                   checked/>
                        </div>
                        <div class="col-lg-6 col-md-12 col-sm-6">
                            <h5>Non-labeled Radio</h5>
                            <input class="to-labelauty-icon" type="radio" name="rd4" checked/>
                            <input class="to-labelauty-icon" type="radio" name="rd4"/>
                            <input class="to-labelauty-icon" type="radio" name="rd3" disabled checked/>
                        </div>

                    </div>
                </div>
            </div>
        </div>
        <div class="col-md-6">
            <div class="card ">
                <div class="card-header">
                    <h3 class="card-title">
                        <i class="fa fa-fw ti-check"></i> jQuery prettyCheckable
                    </h3>
                    <span class="float-right txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                </div>
                <div class="card-body">
                    <div class="form-group">
                        <label for="Test1">Right positioned label</label>
                        <input type="checkbox" class="test1" value="1" id="Test1" name="Test1" checked/>
                    </div>
                    <div class="form-group">
                        <input type="checkbox" class="TestDisabled" value="3" id="TestDisabled"
                               name="TestDisabled" disabled data-label='Disabled Checkbox'>
                    </div>
                    <div class="form-group">
                        <input type="checkbox" class="test2" value="2" id="Test2" name="Test2"
                               data-label="Left positioned label" data-labelPosition="left"/>
                    </div>
                    <div class="form-group">
                        <label class="test_radio">Radios! </label>
                        <input type="radio" class="test3" value="1" id="Test3_0" name="Test3" data-label="Yes"
                               checked data-customclass="margin-right"/>
                        <input type="radio" class="test4" value="2" id="Test3_1" name="Test3" data-label="No"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="row">
        <div class="col-md-12">
            <div class="card ">
                <div class="card-header">
                    <h3 class="card-title">
                        <i class="fa fa-fw ti-arrow-circle-up"></i> Awesome Radio &amp; Checkbox
                    </h3>
                    <span class="float-right txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                </div>
                <div class="card-body">
                    <div class="box-body">
                        <div class="row">
                            <div class="col-md-6 col-sm-6 awesomeradio_grid_sep">
                                <div class="row">
                                    <div class="col-md-12">
                                        <h5>Checkboxes</h5>
                                        <div class="col-md-12">
                                            <div class="row">
                                                <div class="col-lg-4 col-sm-6 marginLeft">
                                                    <div class="checkbox checkbox-default">
                                                        <input id="checkbox1" class="styled styled1" type="checkbox">
                                                        <label for="checkbox1">
                                                            &nbsp;Default
                                                        </label>
                                                    </div>
                                                </div>
                                                <div class="col-lg-4 col-sm-6 marginLeft">
                                                    <div class="checkbox checkbox-primary">
                                                        <input id="checkbox2" class="styled styled1" type="checkbox">
                                                        <label for="checkbox2" class="marginTop">
                                                            &nbsp;Primary
                                                        </label>
                                                    </div>
                                                </div>
                                                <div class="col-lg-4 col-sm-6 marginLeft">
                                                    <div class="checkbox checkbox-success">
                                                        <input id="checkbox3" class="styled styled1" type="checkbox">
                                                        <label for="checkbox3" class="marginTop">
                                                            &nbsp;Success
                                                        </label>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-md-12">
                                            <div class="row">
                                                <div class="col-lg-4 col-sm-6 marginLeft">
                                                    <div class="checkbox checkbox-info">
                                                        <input id="checkbox4" class="styled styled1" type="checkbox">
                                                        <label for="checkbox4">
                                                            &nbsp;Info
                                                        </label>
                                                    </div>
                                                </div>
                                                <div class="col-lg-4 col-sm-6 marginLeft">
                                                    <div class="checkbox checkbox-warning">
                                                        <input id="checkbox5" class="styled styled1" type="checkbox">
                                                        <label for="checkbox5" class="marginTop">
                                                            &nbsp;Warning
                                                        </label>
                                                    </div>
                                                </div>
                                                <div class="col-lg-4 col-sm-6 marginLeft">
                                                    <div class="checkbox checkbox-danger">
                                                        <input id="checkbox6" class="styled styled1" type="checkbox">
                                                        <label for="checkbox6" class="marginTop">
                                                            &nbsp;Danger
                                                        </label>
                                                    </div>
                                                </div>
                                            </div>

                                        </div>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-md-12 mt-3">
                                        <h5>Inline checkboxes</h5>
                                        <div class="inline-response">
                                        <div class="row">
                                                <div class="col-lg-4 col-sm-6">
                                                    <div class="checkbox checkbox-inline m-l-18">
                                                        <input type="checkbox" class="styled" id="inlineCheckbox1"
                                                               value="option1">
                                                        <label for="inlineCheckbox1"> &nbsp;Inline One </label>
                                                    </div>
                                                </div>
                                                <div class="col-lg-4 col-sm-6">
                                                    <div class="checkbox checkbox-inline m-l-18">
                                                        <input type="checkbox" class="styled" id="inlineCheckbox2"
                                                               value="option1">
                                                        <label for="inlineCheckbox2"> &nbsp;Inline Two </label>
                                                    </div>
                                                </div>
                                                <div class="col-lg-4 col-sm-6">
                                                    <div class="checkbox checkbox-inline m-l-18">
                                                        <input type="checkbox" class="styled" id="inlineCheckbox3"
                                                               value="option1">
                                                        <label for="inlineCheckbox3">InlineThree</label>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-md-12 mt-3">
                                        <h5>Circled checkboxes</h5>
                                        <div class="inline-response">
                                        <div class="row">
                                            <div class="col-md-6">
                                                <div class="checkbox checkbox-circle">
                                                    <input id="checkbox7" class="styled" type="checkbox">
                                                    <label for="checkbox7">Simply Round</label>
                                                </div>
                                            </div>
                                            <div class="col-md-6">
                                                <div class="checkbox checkbox-info checkbox-circle">
                                                    <input id="checkbox8" class="styled styled1" type="checkbox">
                                                    <label for="checkbox8">
                                                        &nbsp;Me too
                                                    </label>
                                                </div>
                                            </div>
                                        </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-md-12 mt-3">
                                        <h5>
                                            Disabled
                                        </h5>
                                        <div class="inline-response">
                                        <div class="row">
                                            <div class="col-lg-4 col-sm-4">
                                                <div class="checkbox">
                                                    <input class="styled" id="checkbox9" type="checkbox"
                                                           disabled>
                                                    <label for="checkbox9">
                                                        &nbsp;Can't check
                                                    </label>
                                                </div>
                                            </div>
                                            <div class="col-lg-4 col-sm-4">
                                                <div class="checkbox checkbox-success">
                                                    <input class="styled styled" id="checkbox10" type="checkbox"
                                                           disabled checked>
                                                    <label for="checkbox10">
                                                        &nbsp;This too
                                                    </label>
                                                </div>
                                            </div>
                                            <div class="col-lg-4 col-sm-4">
                                                <div class="checkbox checkbox-warning checkbox-circle">
                                                    <input class="styled" id="checkbox11" type="checkbox"
                                                           disabled checked>
                                                    <label for="checkbox11">
                                                        &nbsp;And this
                                                    </label>
                                                </div>
                                            </div>
                                        </div>
                                        </div>
                                    </div>
                                </div>

                            </div>
                            <div class="col-md-6 col-sm-6">
                                <div class="row">
                                    <div class="col-md-12 mb-3">
                                        <h5>Radios</h5>
                                        <div class="row">
                                            <div class="col-sm-6">
                                                <div class="radio">
                                                    <input type="radio" name="radio1" id="radio1"
                                                           value="option1">
                                                    <label for="radio1">Small</label>
                                                </div>
                                                <div class="radio">
                                                    <input type="radio" name="radio1" id="radio2"
                                                           value="option2">
                                                    <label for="radio2">Big</label>
                                                </div>
                                            </div>
                                            <div class="col-sm-6">
                                                <div class="radio radio-danger">
                                                    <input type="radio" name="radio2" id="radio3"
                                                           value="option1">
                                                    <label for="radio3">Next</label>
                                                </div>
                                                <div class="radio radio-danger">
                                                    <input type="radio" name="radio2" id="radio4"
                                                           value="option2">
                                                    <label for="radio4">One</label>
                                                </div>
                                            </div>
                                        </div></div>
                                </div>
                                <div class="row">
                                    <div class="col-md-12 mb-3">
                                        <h5>
                                            Disabled state
                                        </h5>
                                        <div class="row">
                                            <div class="col-md-6">
                                                <div class="radio radio-danger">
                                                    <input type="radio" name="radio3" id="radio5"
                                                           value="option1" disabled>
                                                    <label for="radio5">Next</label>
                                                </div>
                                            </div>
                                            <div class="col-md-6">
                                                <div class="radio">
                                                    <input type="radio" name="radio3" id="radio6"
                                                           value="option2" checked disabled>
                                                    <label for="radio6">
                                                        &nbsp;One
                                                    </label>
                                                </div>
                                            </div>
                                        </div></div>
                                </div>
                                <div class="row">
                                    <div class="col-md-12 mb-3">
                                        <h5>Inline radios</h5>
                                        <div class="inline-response">
                                        <div class="row">
                                            <div class="col-md-6">
                                                <div class="radio radio-info radio-inline m-l-18">
                                                    <input type="radio" id="inlineRadio1" value="option1"
                                                           name="radioInline">
                                                    <label for="inlineRadio1"> &nbsp;Inline One </label>
                                                </div>
                                            </div>
                                            <div class="col-md-6">
                                                <div class="radio radio-inline m-l-18">
                                                    <input type="radio" id="inlineRadio2" value="option2"
                                                           name="radioInline">
                                                    <label for="inlineRadio2"> &nbsp;Inline Two </label>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    </div>
                                    </div>
                                <div class="row">
                                    <div class="col-md-12 mb-3">
                                        <h5>
                                            Radio As Checkboxes
                                        </h5>
                                        <div class="checkbox  checkbox-inline checkbox-default">
                                            <input type="radio" name="radio4" id="radio7" value="option1"
                                                   checked>
                                            <label for="radio7">
                                                &nbsp;Default
                                            </label>
                                        </div>
                                        <div class="checkbox  checkbox-inline checkbox-success">
                                            <input type="radio" name="radio4" id="radio8" value="option2">
                                            <label for="radio8">
                                                &nbsp;<span>Success</span>
                                            </label>
                                        </div>
                                        <div class="checkbox  checkbox-inline checkbox-danger">
                                            <input type="radio" name="radio4" id="radio9" value="option3">
                                            <label for="radio9">
                                                &nbsp;<span>Danger</span>
                                            </label>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!--main content ends-->
</div>
</template>
<script>
import prettyCheckable from "../../vendors/prettyCheckable/dist/prettyCheckable.min.js"
import labeluty from "../../vendors/jquery-labelauty/source/jquery-labelauty.js"

export default {
    name: "radio_check",
    data(){
        return   {
        message: '',
        search:'',
        isActive:false,
        drinks:[{
            name:'Coffee',
            active:false
        },
            {
                name:'Tea',
                active:false
            },{
                name:'Milk',
                active:false
            },{
                name:'Juice',
                active:false
            },{
                name:'Milk shakes',
                active:false
            },{
                name:'Cool Drink',
                active:false
            },{
                name:'Water',
                active:false
            },{
                name:'Butter Milk',
                active:false
            }]
    }},
    mounted: function() {
        "use strict";
        $(document).ready(function() {
            $('input.test1').prettyCheckable({});
            $('input.TestDisabled').prettyCheckable({});
            $('input.test2').prettyCheckable({});
            $('input.test3').prettyCheckable({});
            $('input.test4').prettyCheckable({});

            $(".to-labelauty").labelauty({
                minimum_width: "155px"
            });
            $(".to-labelauty-icon").labelauty({
                label: false
            });
        });
    },
    destroyed: function() {
    },
    methods: {
        changeState() {
            var el = document.getElementById("indeterminateCheckbox");
            if (el.readOnly) el.checked = el.readOnly = false;
            else if (!el.checked) el.readOnly = el.indeterminate = true;
        },
    },
    computed:{
        allDrinks:function()
        {
            var self=this;
            return this.drinks.filter(function(drinky){return drinky.name.toLowerCase().indexOf(self.search.toLowerCase())>=0;});
            //return this.customers;
        }
    }
}


</script>
<style src="../../vendors/prettyCheckable/dist/prettyCheckable.css"></style>
<style src="../../assets/css/jquery-labelauty.css"></style>
<style src="../../vendors/awesome-bootstrap-checkbox/awesome-bootstrap-checkbox.css"></style>
<style src="../../assets/css/custom_css/radio_checkbox.css"></style>
