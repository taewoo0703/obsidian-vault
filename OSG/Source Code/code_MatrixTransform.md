```cpp
/* -*-c++-*- O[penSceneGraph - Copyright (C) 1998-2006 Robert Osfield
 *
 * This library is open source and may be redistributed and/or modified under
 * the terms of the OpenSceneGraph Public License (OSGPL) version 0.0 or
 * (at your option) any later version.  The full license is in LICENSE file
 * included with this distribution, and on the openscenegraph.org website.
 *]()
 * This library is distributed in the hope that it will be useful,
 * but WITHOUT ANY WARRANTY; without even the implied warranty of
 * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 * OpenSceneGraph Public License for more details.
*/

#ifndef OSG_MATRIXTRANSFORM
#define OSG_MATRIXTRANSFORM 1

#include <osg/Transform>

namespace osg {
/** MatrixTransform - is a subclass of Transform which has an osg::Matrix
  * which represents a 4x4 transformation of its children from local coordinates
  * into the Transform's parent coordinates.
*/
class OSG_EXPORT MatrixTransform : public Transform
{
    public :
        MatrixTransform();
        /** Copy constructor using CopyOp to manage deep vs shallow copy.*/
        MatrixTransform(const MatrixTransform&,const CopyOp& copyop=CopyOp::SHALLOW_COPY);
        MatrixTransform(const Matrix& matix);
        META_Node(osg, MatrixTransform);
        virtual MatrixTransform* asMatrixTransform() { return this; }
        virtual const MatrixTransform* asMatrixTransform() const { return this; }
        
        /** Set the transform's matrix.*/
        void setMatrix(const Matrix& mat) { _matrix = mat; _inverseDirty=true; dirtyBound(); }

        /** Get the matrix. */
        inline const Matrix& getMatrix() const { return _matrix; }

        /** pre multiply the transform's matrix.*/
        void preMult(const Matrix& mat) { _matrix.preMult(mat); _inverseDirty=true; dirtyBound(); }
        
        /** post multiply the transform's matrix.*/
        void postMult(const Matrix& mat)  { _matrix.postMult(mat); _inverseDirty=true; dirtyBound(); }
  
        /** Get the inverse matrix. */
        inline const Matrix& getInverseMatrix() const
        {
            if (_inverseDirty)
            {
                _inverse.invert(_matrix);
                _inverseDirty = false;
            }
            return _inverse;
        }
        virtual bool computeLocalToWorldMatrix(Matrix& matrix,NodeVisitor*) const;
        virtual bool computeWorldToLocalMatrix(Matrix& matrix,NodeVisitor*) const;
        
    protected :
        virtual ~MatrixTransform();
        Matrix                              _matrix;
        mutable Matrix                      _inverse;
        mutable bool                        _inverseDirty;
};
}
#endif
```