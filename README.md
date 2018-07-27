# TelerikReporting_AspNetCore_ReportViewer


This Telerik ASP.NET Core (2.0) MVC Application implements an instance of the Telerik Reporting HTML5 Report Viewer in a C# Razor View and provides code to toggle between setting the service URL (provides report content to viewer) to an instance of the ReportingRestServiceCors implementation (available at https://github.com/rzaslaw/ReportingRestServiceCors) or an instance of the Telerik Report Server (see https://www.telerik.com/report-server) that needs to be licensed seperately from Telerik Reporting SDK. 

    <script>
        $(document).ready(function () {
            $("#reportViewer1")
                .telerik_ReportViewer({
                    //reportServer: { "url": "http://myreportserver:port/", "username": "*****", "password": "*****" },
                   // reportSource: { report: "Samples/Product Line Sales.trdp", parameters: {} },
                    serviceUrl: "http://localhost/ReportingRestServiceCors/api/Reports/",
                    reportSource: { report: "Dashboard.trdp", parameters: {} },
                    scale: 1.0,
                    persistSession: false,
                    parametersAreaVisible: true,
                    documentMapVisible: true,
                    viewMode: "INTERACTIVE",
                    scaleMode: "SPECIFIC",
                    printMode: "AUTO_SELECT"
                });
        });
    </script> 

This topic (https://docs.telerik.com/reporting/html5-report-viewer-embedding#manual-setup) shows you how to add the HTML5 Report Viewer to HTML page and display a report in it.