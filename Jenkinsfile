node {
   echo 'Hello World'
}
   String[][] buildChains = [
  ['master'],
  ['branch1', 'master'],
  ['branch2', 'branch1', 'master'],
  ['no-build']
  ]

for ( buildChain in buildChains ) {
  if ( buildChain[0].equalsIgnoreCase( env.BRANCH_NAME ) ) {
    int depth = 0
    for ( branch in buildChain ) {
      String depthIndicator = "+" * ++depth
      println "  $depthIndicator Triggering build for branch '$branch'"
      build( branch )
      } 
    break 
    }
  } 


def build( String branch ) {

  switch ( branch ) {
    case "master":
      buildMaster()
      break
    case ["branch1", "branch2"]:
      buildBranch( branch )
      break
    default:
      println "  --- No build defined for branch \'$branch\' ---"
    }  
  }  

def buildMaster()   {
  println '  Building branch \'master\'...'
  }

def buildBranch( String branch )    {
  println "  Building branch '$branch'..."
  }
String repeat( String s, int count ) {
  return count > 0 ? s + repeat( s, --count ) : ""
  }

