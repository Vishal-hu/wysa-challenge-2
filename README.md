# wysa-challenge-2
## BST validator

``` const isValidBST = (root) => {
    let output = true;
    const loop = (tree, min, max) => {
        if ((tree?.val > min || min === undefined) && (tree?.val < max || max === undefined)) {
            if (tree?.left) {
                loop(tree.left, min, tree.val);    
            }
            if (tree?.right) {
                loop(tree.right, tree.val, max);    
            }
        } else {
            output = false;
        }
    }
    loop(root);
    return output;
}; ```
