# Unit Tests

    a. When updating any file in the  src/public/simpleui-server  folder
    b. When updating the server side of zmq communications.

1. From the "npm" Tool Window, double-click "test-simpleui-server",
   or from the command line in the ng-simple-ui folder, execute the command below:

           bash src/public/simpleui-server/test/simpleui-server.unit-test.bash

2. In the "Run" window of phpstorm, look at the "Summary" for the "Failed tests" line.

   a. If "Failed tests" is not 0, the unit test failed.

   b. If "failed on nodejs:" is not 0, you must fix a crash in the typescript code
      and rerun from step 1.

   c. If "failed on diff:" is not 0, you must fix the logic in the typescript code
      and rerun from step 1.

      In this case, look above for "RESULT: diff test failed".
       i. Compare the two "pretty" files" created when a diff test fails:
              [STUB].out.reference.pretty.json
              [STUB].out.test.pretty.json

      ii. If the changes in [STUB].out.test.pretty.json are expected due to code changes,
          copy the non-pretty .out.test.json file to .out.reference.json and CHECK IN.
          Do NOT check in [STUB].out.test.json or any pretty.json files.

              cp [STUB].out.test.json [STUB].out.reference.json

     iii. If the changes in [STUB].out.test.pretty.json are NOT expected , fix the
          typescript code and rerun from step 1.