Find:

    ^([A-Z][a-z\s,]+\?)\s?+$
    
Replace:

    it\('$1', Function\(\)\);

Find:

    '([A-Z][a-z]+)(\s)([A-Z][a-z]+)'
    
Replace:

    describe\('$1$2$3', $1$3\);

Find:

    var foo = document.body.innerHTML.match(/E_COMPILE_ERROR[^)]+/g)
    
Replace:

    var bar = foo.map(function(value, index){return value.replace(/\n\s+/,"")})
