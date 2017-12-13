<template>
    <div>
        <div class="row">
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> Default Date Picker
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">
                        <datepicker placeholder="Select Date"></datepicker>
                        <code>
                            &lt;datepicker&gt;&lt;/datepicker&gt;
                        </code>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> V-Calendar Date Picker
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">

                        <h5> Date With Range Selector</h5>
                        <v-date-picker
                                :mode='mode'
                                :select-color='selectColor'
                                :drag-color='dragColor'
                                :disabled-dates='showDisabledDates ? disabledDates : null'
                                :attributes='[todayAttribute]'
                                :is-inline='isInline'
                                :popover-visibility='popoverVisibility'
                                :popover-direction='popoverDirection'
                                :popover-align='popoverAlign'
                                indicators-offset='4px'
                                inputClass='input'
                                v-model='selectedValue2'
                                is-double-paned
                                is-expanded>
                        </v-date-picker>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> Translations
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">
                        <h5>Spanish datepicker</h5>
                        <datepicker language="es"></datepicker>
                        <code>
                            &lt;datepicker language="es"&gt;&lt;/datepicker&gt;
                        </code>
                        <h5>French datepicker</h5>
                        <datepicker language="fr"></datepicker>
                        <code>
                            &lt;datepicker language="fr"&gt;&lt;/datepicker&gt;
                        </code>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> Date Format
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">
                        <datepicker :format="format"></datepicker>
                        <code>
                            &lt;datepicker :format="format"&gt;&lt;/datepicker&gt;
                        </code>
                        <div class="settings">
                            <h5>Settings</h5>
                            <div class="form-group">
                                <label class="label_font">Format</label>
                                <select v-model="format">
                                    <option value="d MMM yyyy" selected>d MMM yyyy - e.g 12 Feb 2016</option>
                                    <option value="d MMMM yyyy">d MMMM yyyy - e.g 12 February 2016</option>
                                    <option value="yyyy-MM-dd">yyyy-MM-dd - e.g 2016-02-12</option>
                                    <option value="dsu MMM yyyy">dsu MMM yyyy - e.g 12th Feb 2016</option>
                                    <option value="D dsu MMM yyyy">D dsu MMM yyyy - e.g Sat 12th Feb 2016</option>
                                </select>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> With minimum and maximum date range
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">
                        <datepicker :disabled="disabled"></datepicker>
                        <code>
                            &lt;datepicker :disabled="disabled"&gt;&lt;/datepicker&gt;
                        </code>
                        <div class="settings ">
                            <h5 class="mt-2">Settings</h5>
                            <div class="form-group">
                                <label class="label_font">Range from:</label>
                                <datepicker @selected="disableTo"></datepicker>
                            </div>
                            <div class="form-group">
                                <label class="label_font">Range to:</label>
                                <datepicker @selected="disableFrom"></datepicker>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> Inline datepicker
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body full_calendar">
                        <datepicker :inline="true"></datepicker>
                        <code>
                            &lt;datepicker :inline="true"&gt;&lt;/datepicker&gt;
                        </code>
                    </div>
                </div>
            </div>
            <div class="col-md-12 col-lg-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> V-Calendar Highlight Style
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">
                        <v-calendar :attributes='high_attributes' is-double-paned class="mb-3">
                        </v-calendar>
                    </div>
                </div>
            </div>
            <div class="col-md-12 col-lg-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> V-Calendar Dot Style
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">
                        <v-calendar :attributes='dot_attributes' is-double-paned class="mb-3">
                        </v-calendar>
                    </div>
                </div>
            </div>
            <div class="col-md-12 col-lg-6">
                <div class="card">
                    <div class="card-header txt_padding">
                        <h3 class="card-title">
                            <i class="ti-calendar"></i> V-Calendar Content Style
                        </h3>
                        <span class="float-right fnt_size txt_font">
                                    <i class="fa fa-fw ti-angle-up clickable"></i>
                                    <i class="fa fa-fw ti-close removecard"></i>
                                </span>
                    </div>
                    <div class="card-body">
                        <v-calendar :attributes='content_attributes' is-double-paned class="mb-3">
                        </v-calendar>
                    </div>
                </div>
            </div>


        </div>
    </div>

</template>
<script>
    import Vue from 'vue';
    import VCalendar from 'v-calendar';
    import 'v-calendar/lib/v-calendar.min.css';
    import {getExampleMonthComps} from 'v-calendar/src/utils/helpers'

    import MaskedInput from 'vue-masked-input'
    import Datepicker from 'vuejs-datepicker'
    Vue.use(VCalendar);
    var state = {
        date1: new Date()
    }
    const {
        thisMonth,
        thisMonthYear,
        nextMonth,
        nextMonthYear } = getExampleMonthComps();


    export default {
        props: {
            mode: { type: String, default: 'range' },
            selectColor: { type: String, default: '#66b3cc' },
            dragColor: { type: String, default: '#9fcfdf' },
            showDisabledDates: Boolean,
            isInline: Boolean,
            isExpanded: Boolean,
            popoverVisibility: { type: String, default: 'hover' },
            popoverDirection: { type: String, default: 'bottom' },
            popoverAlign: { type: String, default: 'left' },
        },
        components: {
            Datepicker,
            MaskedInput,
//            VCalendar
        },
        data() {
            return {
                format: 'd MMMM yyyy',
                disabled: {},
                eventMsg: null,
                state: state,
                date:'',
                date2:'',
                phone:'',
                intlphone:'',
                ip:'',
                high_attributes:[{
                    highlight: {
                        backgroundColor: '#ff8080', // Red
                        borderColor: '#ff6666',
                        borderWidth: '2px',
                        borderStyle: 'solid',
                    },
                    contentStyle: {
                        color: 'white',
                    },
                    dates: [
                        // Use date ranges
                        {
                            start: new Date(thisMonthYear, thisMonth, 1),
                            end: new Date(thisMonthYear, thisMonth, 4),
                        },
                        // Or single dates
                        new Date(nextMonthYear, nextMonth, 6),
                        new Date(nextMonthYear, nextMonth, 23),
                    ],
                },
                    {
                        highlight: {
                            backgroundColor: '#9f80ff', // Purple
                            borderColor: '#8c66ff',
                            borderWidth: '2px',
                        },
                        contentStyle: {
                            color: 'white',
                        },
                        dates: [
                            new Date(thisMonthYear, thisMonth, 1),
                            new Date(thisMonthYear, thisMonth, 10),
                            new Date(thisMonthYear, thisMonth, 12),
                            {
                                start: new Date(nextMonthYear, nextMonth, 22),
                                end: new Date(nextMonthYear, nextMonth, 26),
                            },
                        ],
                    }
                ],
                dot_attributes: [
                    {
                        dot: {
                            backgroundColor: '#ff4d4d', // Red
                        },
                        dates: [
                            new Date(thisMonthYear, thisMonth, 1),
                            new Date(thisMonthYear, thisMonth, 10),
                            new Date(thisMonthYear, thisMonth, 22),
                            new Date(nextMonthYear, nextMonth, 6),
                            new Date(nextMonthYear, nextMonth, 16),
                        ],
                    },
                    {
                        dot: {
                            backgroundColor: '#398fac', // Turquoise
                        },
                        dates: [
                            new Date(thisMonthYear, thisMonth, 4),
                            new Date(thisMonthYear, thisMonth, 10),
                            new Date(thisMonthYear, thisMonth, 15),
                            new Date(nextMonthYear, nextMonth, 1),
                            new Date(nextMonthYear, nextMonth, 12),
                            {
                                start: new Date(nextMonthYear, nextMonth, 20),
                                end: new Date(nextMonthYear, nextMonth, 25),
                            },
                        ],
                    }
                ],
                content_attributes: [
                    {
                        contentStyle: {
                            color: '#ff4d4d', // Red
                            fontWeight: 600,
                            fontSize: '1em',
                        },
                        dates: [
                            {
                                start: new Date(thisMonthYear, thisMonth, 1),
                                end: new Date(thisMonthYear, thisMonth, 4),
                            },
                            new Date(nextMonthYear, nextMonth, 6),
                            new Date(nextMonthYear, nextMonth, 23),
                        ],
                    },
                    {
                        contentStyle: {
                            color: '#398fac', // Turquoise
                            fontWeight: 600,
                            fontStyle: 'italic',
                        },
                        dates: [
                            new Date(thisMonthYear, thisMonth, 1),
                            new Date(thisMonthYear, thisMonth, 10),
                            new Date(thisMonthYear, thisMonth, 12),
                            {
                                start: new Date(nextMonthYear, nextMonth, 22),
                                end: new Date(nextMonthYear, nextMonth, 26),
                            },
                        ],
                    },
                    {
                        contentStyle: {
                            color: '#794dff', // Purple
                            fontWeight: 600,
                        },
                        dates: [
                            new Date(thisMonthYear, thisMonth, 14),
                            {
                                start: new Date(thisMonthYear, thisMonth, 24),
                                end: new Date(thisMonthYear, thisMonth, 25),
                            },
                            new Date(thisMonthYear, thisMonth, 28),
                            new Date(thisMonthYear, thisMonth + 1, 4),
                            {
                                start: new Date(nextMonthYear, nextMonth, 16),
                                end: new Date(nextMonthYear, nextMonth, 17),
                            },
                        ],
                    },
                ],
                selectedValue2: {
                    start: new Date(thisMonthYear, thisMonth, 6),
                    end: new Date(nextMonthYear, nextMonth, 25),
                },
                disabledDates: [
                    {
                        start: new Date(nextMonthYear, nextMonth, 26),
                        end: new Date(nextMonthYear, nextMonth, 28),
                    },
                ],
                todayAttribute: {
                    contentStyle: {
                        color: '#ffffff',
                        backgroundColor: '#ff9999',
                        border: 'solid 1px #ff8080',
                        fontWeight: 600,
                    },
                    dates: [new Date()],
                },

            }
        },
        methods: {
            disableTo(val) {
                console.log(val)
                if (typeof this.disabled.to === 'undefined') {
                    this.disabled = {
                        to: null,
                        from: this.disabled.from
                    };
                }
                this.disabled.to = val;
            },
            disableFrom(val) {
                if (typeof this.disabled.from === 'undefined') {
                    this.disabled = {
                        to: this.disabled.to,
                        from: null
                    };
                }
                this.disabled.from = val;
            }
        }
    }
</script>
<style scoped>
    code,
    pre {
        margin: 1em 0;
        padding: 1em;
        border: 1px solid #bbb;
        display: block;
        background: #f1f1f1;
        border-radius: 3px;
    }

    .settings {
        margin: 2em 0;
        /*padding: 0 1.5em 1.5em;*/
        background: #fff;
    }

    h5 {
        font-size: 100%;
        padding: 0;
    }

    .form-group {
        margin-bottom: 1em;
    }

    .form-group label {
        font-size: 80%;
        display: block;
    }

    select {
        height: 2.5em;
        padding: 0;
    }

</style>
<style>
    .example .vdp-datepicker__calendar{
        margin: 0 auto;
    }
    .label_font{
        font-size: 12px !important;
    }
    .vdp-datepicker input{
        padding: 0.75rem 0.5rem;
        width: 100%;
    }
    .vdp-datepicker .vdp-datepicker__calendar{
        margin: auto;
    }
    .c-pane-container.is-double-paned,.c-pane-container,.settings select{
        width: 100% !important;
    }
    .full_calendar .vdp-datepicker__calendar{
        margin-left:0 !important;
        width:100%!important;
    }
    .popover-container input{
        width: 100%;
        padding: 0.5rem;
        border-radius: 5px;
        border: 1px solid #A9A9A9;
    }
    .usetweentyfour{
        margin-left: -20px;
    }
    @media(max-width: 768px){
        .c-pane-container.is-double-paned{
            margin-left: -8px;
        }
    }
    @media (min-width: 720px) and (max-width: 1024px){
        .popover-origin .popover-content-wrapper .popover-content.direction-bottom{
            left: -15px;
        }
    }
    @media(min-width:320px) and (max-width: 768px){
        .vdp-datepicker__calendar{
            width: 265px !important;
            margin-left: -20px !important;
        }
    }
    .c-pane-container.is-double-paned{
        min-width:100px !important;
    }


</style>
