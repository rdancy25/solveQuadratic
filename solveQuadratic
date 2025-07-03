function roots = solveQuadratic(a, b, c)
% solveQuadratic finds the real roots of a quadratic equation ax^2 + bx + c = 0.
%
%   ROOTS = solveQuadratic(a, b, c) returns a vector containing the real
%   roots of the equation defined by coefficients a, b, and c.
%
%   - If two real roots exist, it returns a 1x2 sorted vector.
%   - If one real root exists, it returns a scalar.
%   - If no real roots exist (i.e., roots are complex), it returns an empty vector.
%
%   The function will throw an error if 'a' is zero, as the equation would
%   not be quadratic.

% Validate that the equation is actually quadratic
if a == 0
    error('Coefficient ''a'' cannot be zero for a quadratic equation.');
end

% Calculate the discriminant
discriminant = b^2 - 4*a*c;

% Determine the nature of the roots based on the discriminant
if discriminant > 0
    % Two distinct real roots
    r1 = (-b + sqrt(discriminant)) / (2*a);
    r2 = (-b - sqrt(discriminant)) / (2*a);
    roots = sort([r1, r2]); % Return sorted roots
elseif discriminant == 0
    % One real root
    roots = -b / (2*a);
else
    % No real roots (complex roots)
    roots = [];
end

end
