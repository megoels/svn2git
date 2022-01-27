svn2git
=======

Forked from: http://github.com/nirvdrum/svn2git (check for installing and usage)  
The ruby package wasn't uploaded to rubygems therefore you will need to install according to above,  
After that you may replace migration.rb at ruby gems.  
For example at windows:  
Copy the lib/svn2git/migration.rb to C:\Ruby30\lib\ruby\gems\3.0.0\gems\svn2git-2.4.0\lib\svn2git  

Options Reference (Extended)
----------------------------

    $ svn2git --help
    Usage: svn2git SVN_URL [options]
    
    Specific options:
            --rebase                     Instead of cloning a new project, rebase an existing one against SVN
            --username NAME              Username for transports that needs it (http(s), svn)
            --password PASSWORD          Password for transports that need it (http(s), svn)
            --trunk TRUNK_PATH           Subpath to trunk from repository URL (default: trunk)
            --branches BRANCHES_PATH     Subpath to branches from repository URL (default: branches); can be used multiple times
            --branch BRANCH_PATH         Path to single branch from repository URL; can be used multiple times
            --tags TAGS_PATH             Subpath to tags from repository URL (default: tags); can be used multiple times
            --rootistrunk                Use this if the root level of the repo is equivalent to the trunk and there are no tags or branches
            --notrunk                    Do not import anything from trunk
            --nobranches                 Do not try to import any branches
            --notags                     Do not try to import any tags
            --no-minimize-url            Accept URLs as-is without attempting to connect to a higher level directory
            --revision START_REV[:END_REV]
                                        Start importing from SVN revision START_REV; optionally end at END_REV
        -m, --metadata                   Include metadata in git logs (git-svn-id)
            --authors AUTHORS_FILE       Path to file containing svn-to-git authors mapping (default: ~/.svn2git/authors)
            --exclude REGEX              Specify a Perl regular expression to filter paths when fetching; can be used multiple times
        -v, --verbose                    Be verbose in logging -- useful for debugging issues
            --rebasebranch REBASEBRANCH  Rebase specified branch.
        -o, --only-branches-at-rootbar   Only the name branches will be at git root others in folders, e.g: releases will store branches under releases git folder
            --skip-init                  Use only in case need to continue post the init

        -h, --help                       Show this message