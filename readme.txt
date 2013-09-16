//
// This is a basic sample using "msnodesql" Microsofts Nodejs driver for MS SQL
// including the current version of msnodesql _with_ compiled binaries for Node 0.10 (current) & x64 
// which you otherwise need to compile for yourself if you like to use the driver.
// Until Microsoft updated the binaries themselfes, vote for that to happen att the
// issue tracker on the drive repository: https://github.com/WindowsAzure/node-sqlserver/issues/126
//
// Working sample code:
//

var sql = require('msnodesql');

var conn_str = "Driver={SQL Server Native Client 11.0};Server={(local)\\SQLEXPRESS};Database={somedb};Trusted_Connection={Yes};";

	sql.open(conn_str, function( err, conn ) {

		console.log(err);

		conn.query( "SELECT * FROM dbo.sometable", function( err, results ) {
			console.log(results);
		});


	});
