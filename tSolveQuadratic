classdef tSolveQuadratic < matlab.unittest.TestCase
    % testSolveQuadratic contains unit tests for the solveQuadratic function.

    methods (Test)
        % Test case for a standard equation with two distinct real roots
        function testTwoRealRoots(testCase)
            % For x^2 - 5x + 6 = 0, roots are 2 and 3
            a = 1; b = -5; c = 6;
            expectedRoots = [2, 3];
            actualRoots = solveQuadratic(a, b, c);
            testCase.verifyEqual(actualRoots, expectedRoots);
        end

        % Test case for an equation with one real root
        function testOneRealRoot(testCase)
            % For x^2 - 6x + 9 = 0, root is 3
            a = 1; b = -6; c = 9;
            expectedRoot = 3;
            actualRoot = solveQuadratic(a, b, c);
            testCase.verifyEqual(actualRoot, expectedRoot);
        end

        % Test case for an equation with no real roots (complex roots)
        function testNoRealRoots(testCase)
            % For x^2 + 2x + 5 = 0, discriminant is negative
            a = 1; b = 2; c = 5;
            actualRoots = solveQuadratic(a, b, c);
            testCase.verifyEmpty(actualRoots, ...
                'Function should return an empty array for complex roots.');
        end
       
        % Test case with floating-point coefficients and roots
        function testFloatingPointRoots(testCase)
            % For 2x^2 - x - 3 = 0, roots are -1 and 1.5
            a = 2; b = -1; c = -3;
            expectedRoots = [-1, 1.5];
            actualRoots = solveQuadratic(a, b, c);
            testCase.verifyEqual(actualRoots, expectedRoots, 'AbsTol', 1e-9);
        end
    end
end
