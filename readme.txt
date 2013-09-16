this is a basic sample using msnodesql, including the current version of msnodesql _with_ compiled binaries on win8x64 

var sql = require('msnodesql');

var conn_str = "Driver={SQL Server Native Client 11.0};Server={(local)\\SQLEXPRESS};Database={somedb};Trusted_Connection={Yes};";

	sql.open(conn_str, function( err, conn ) {

		console.log(err);

		conn.query( "SELECT * FROM dbo.sometable", function( err, results ) {
			console.log(results);
		});


	});
